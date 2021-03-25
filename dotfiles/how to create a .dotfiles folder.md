
## How to create a `.dotfiles` folder 

### Basic steps

1. create the folder in the right location
2. move some configuration files into it
3. link them back to the original location
4. verify that it works!

### Create symbolic links to the original config file locations

You can use the `ln` command on Linux and macOS to create symbolic links from a source file or directory to a new location:

```
# Create a new link called ~/.emacs.d which comes from ~/.dotfiles/.emacs.d
ln -sf ~/.dotfiles/.emacs.d ~/.emacs.d
```

We'll use this to create links back into the home directory of all the configuration files and folders we moved.
