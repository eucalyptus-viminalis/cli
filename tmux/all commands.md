## Commands
Keybind | Command
-|-
`control - b` | Send the prefix key through to the application.
`control - o` | Rotate the panes in the curent window forwards
`control - z` | suspend the tmux client
`!` | break the current pane out of the window
`#` | list all paste buffers
`$` | rename the current session
`&` | kill the current window
`'` | prompt for a window index to select
`(` | switch the attached client to the previous session
`)` | switch the attached client to the next session
`,` | rename the current window
`-` | delete the most recently copied buffer of text
`.` | prompt for an index to move the current window
`:` | enter the tmux command prompt
`;` | move to the previously active pane
`=` | choose which buffer to paste interactively from a list
`?` | list all key bindings
`D` | choose a client to detach
`L` | switch the attached client back to the last session
`[` | enter copy mode to copy text or view the history
`]` | paste the most recently copied buffer of text
`d` | detach the current client
`f` | prompt to search for text in open windows
`i` | display some information about the current window
`l` | move to the previously selected window
`m` | mark the current pane (see select-pane -m)
`M` | clear the marked pane
`n` | change to the next window
`o` | select the next pane in the current window
`p` | change to the previous window
`q` | briefly display pane indexes
`r` | force redraw of the attached client
`s` | select a new session for the attached client interactively
`t` | show the time
`w` | choose the current window interactively
`x` | kill the current pane
`z` | toggle zoom state of the current pane
`{` | swap the current pane with the previous pane
`}` | swap the current pane with the next pane
`~` | show previous messages from tmux, if any
`arrow-keys` | change to the pane in specified direction
`M-1 - M-5` | arrange panes in one of the five preset layouts: even-horizontal, even-vertical, main-horizontal, main-vertical, tiled
`space` | arrange the current window in the next preset layout
`M-n` | move to the next window with a bell or activity marker
`M-o` | rotate the panes in the current window backwards
`M-p` | move to the previous window with a bell or activity marker
`C-arrow-keys` | resize the current pane in steps of one cell
`M-arrow-keys` | resize the current pane in steps of five cells


> key bindings may be changed with the bind-key and unbind-key commands
