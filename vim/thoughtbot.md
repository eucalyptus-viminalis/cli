# Dot
`.` | repeat last command

# Completion
## In Insert Mode
`control - r` | insert text from a register
`control - a` | insert text from register '.'
`control - p` | completion menu (prev)
`control - n` | completion menu (next)
`control - x` | special "completion mode" submode of insert

### In Completion Mode
`control - ]` | tag completion
`control - p` | pull from previous context
`control - n` | pull from next context
`control - f` | file completion
`control - l` | line completion
`control - o` | omni-completion

# Navigation
## Jumping Lines
`j` | down one line
`k` | up one line
`gg` | first line
`G` | last line
`Ngg` | Nth line

`H` | top of the screen
`M` | middle of the screen
`L` | bottom of the screen

`zt` | display current line at top of the screen
`zz` | display current line at middle of the screen
`zb` | display current line at bottom of the screen

`control - e` | scroll one line down
`control - y` | scroll one line up
`control - d` | scroll half-page down
`control - u` | scroll half-page up
`control - f` | scroll full-page down
`control - b` | scroll full-page up

## Within A Line
`0` | beginning of line
`^` | first char of line
`$` | end of line
`g_` | last char of line

## Extra Fun
`N%` | move to a line N% way down a file
`*` | jump to next occurence of word under cursor
`#` | jump to previous occurence of word under cursor

## Word-wise
`e`
`E`
`b`
`B`
`w`
`W`

### Markers
`m`
`M`

`%` | jump to matching parens
