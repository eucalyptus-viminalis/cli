## `osascript`

Shut down without showing a confirmation dialog:

```bash
osascript -e 'tell app "System Events" to shut down'
```

Shut down after showing a confirmation dialog:

```bash
osascript -e 'tell app "loginwindow" to «event aevtrsdn»'
```

Restart without showing a confirmation dialog:

```bash
osascript -e 'tell app "System Events" to restart'
```

Restart after showing a confirmation dialog:

```bash
osascript -e 'tell app "loginwindow" to «event aevtrrst»'
```

Log out without showing a confirmation dialog:

```bash
osascript -e 'tell app "System Events" to  «event aevtrlgo»'
```

Log out after showing a confirmation dialog:

```bash
osascript -e 'tell app "System Events" to log out'
```

Go to sleep (`pmset`):

```bash
pmset sleepnow
```

Go to sleep (AppleScript):

```bash
osascript -e 'tell app "System Events" to sleep'
```

Put displays to sleep (10.9 and later):

```bash
pmset displaysleepnow
```

The four letter codes for the Apple events are listed in `AERegistry.h`.

All System Events commands above send Apple events to the `loginwindow` process. `loginwindow` is sent the same Apple events as above when you log out, restart, shut down, or put the the Mac to sleep normally. See [Technical Q&A QA1134: Programmatically causing restart, shutdown and/or logout](https://developer.apple.com/library/mac/qa/qa1134/_index.html).

According to `man shutdown`, `shutdown -h now` and `shutdown -r now` send processes a `TERM` signal followed by a `KILL` signal.

According to the [Daemons and Services Programming Guide](https://developer.apple.com/library/mac/documentation/MacOSX/Conceptual/BPSystemStartup/Chapters/Lifecycle.html), when you tell `loginwindow` to log out, processes that support sudden termination are sent a `KILL` signal, and processes that don't support sudden termination are terminated in different ways: Cocoa applications receive the `applicationShouldTerminate:` delegate method, foreground applications receive the `kAEQuitApplication` Apple event, background applications receive the `kAEQuitApplication` Apple event followed by a `KILL` signal, and daemons receive a `TERM` signal followed by a `KILL` signal after a few seconds.

## `shutdown`

The command you are after is [shutdown](https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man8/shutdown.8.html). This informs all users that the machine is going to be shutdown and tells all apps to close files etc.

The command takes a parameter `-h`, `-r` or `-s` to shut down, restart or sleep the Mac.

The command has to be run as root so you need to use `sudo`.

e.g. to reboot the machine immediately

```bash
sudo shutdown -r now
```

e.g. to shutdown the machine in 60 minutes

```bash
sudo shutdown -h +60
```

From comments there are two things to be addressed

How shutdown works is by sending a sigterm to all processes which should then deal with that e.g. save open files etc. If they don't exit then they will get sent a SIGKILL which forces them to die with no chance to respond. The signals are not sent via the normal key message queue so Apps have to deal with this separately to the code that gets called from quit on the menu. A good app should call common code from both.

This [other answer](https://apple.stackexchange.com/a/103633/237) shows how to shutdown as if you hit the menu options. But note that apps can cancel this shutdown

## References
https://apple.stackexchange.com/questions/103571/using-the-terminal-command-to-shutdown-restart-and-sleep-my-mac
