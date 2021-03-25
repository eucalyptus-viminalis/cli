---
date: 2022-03-24
---

# missing semester notes on vim (2020)

## notation
control can be notated in a few different ways:
`^V`, Ctrl-V, <C-V>o

## modes
normal: esc
insert: i
replace: r
command-line: :
visual:
	- line: Shift-V
	- block: Ctrl-V

## quitting
:q quits each window
:qa quits all open windows

## visual mode
v: enter visual mode
V: enter visual line mode
Ctrl-V: enter visual block mode
movement keys to select
y: copy

## using modifiers
ci`[`: Change Inside `[` (square brackets)
da`(`: Delete Around `(` (parentheses)

## advanced movements
%: jump between grouping symbols

## search
/: search mode
enter: go to 1st instance
n: go to next
N: go to previous

# a few useful plugins
- fuzzy finder
- visual undo history
- file explorer

## References
[Lecture 3: Editors(vim)
(2020) | YouTube](https://www.youtube.com/watch?v=a6Q8Na575qc&t=1284s&ab_channel=MissingSemester)
[Editors (Vim) | missing
semester](https://missing.csail.mit.edu/2020/editors/)

