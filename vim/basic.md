## nav
      Command | Description
--------------|------------------
       `hjkl` | left, down, up, right
          `0` | _move cursor to start of current line (the one with the cursor)_
          `$` | _move cursor to end of current line_
          `w` | _move cursor to beginning of next word_
          `b` | _move cursor back to beginning of preceding word_
`:0⏎` or `gg` | _move cursor to first line in file_
`:n⏎` or `nG` | _move cursor to line n_
  `:$` or `G` | _move cursor to last line in file_


## exit
Command|Description
-|-
`:x⏎` | _quit vi, writing out modified file to file named in original invocation_
`:wq⏎` | _quit vi, writing out modified file to file named in original invocation_
`:q⏎`| _quit (or exit) vi_
`:q!⏎`|_quit vi even though latest changes have not been saved for this vi call_

## text

#### undo
Command | Description
-|-
`u` | _UNDO WHATEVER YOU JUST DID; a simple toggle_

#### insert
Command | Description
-|-
`i` | _insert text before cursor, until `<ESC>` hit_
`I` | _insert text at beginning of current line, until `<ESC>` hit_
`a` | _append text after cursor, until `<ESC>` hit_
`A` | _append text to end of current line, until `<ESC>` hit_
`o` | _open and put text in a new line below current line, until `<ESC>` hit_
`O` | _open and put text in a new line above current line, until `<ESC>` hit_

#### replace
Command | Description
-|-
`r` | _replace single character under cursor (no `<ESC>` needed)_
`R` | _replace characters, starting with current cursor position, until `<ESC>` hit_
`cw` | _change the current word with new text, starting with the character under cursor, until `<ESC>` hit_
`cNw` | _change N words beginning with character under cursor, until `<ESC>` hit; e.g., c5w changes 5 words_
`C` | _replace the characters in the current line, until `<ESC>` hit_
`cc` | _replace the entire current line, stopping when `<ESC>` is hit_
`Ncc` or `cNc` | _replace the next N lines, starting with the current line, stoppingwhen `<ESC>` is hit_
`~` | swap case


#### delete
Command | Description
-|-
`x` | _delete single character under cursor_
`Nx` | _delete N characters, starting with character under cursor_
`dw` | _delete the single word beginning with character under cursor_
`dNw` | _delete N words beginning with character under cursor; e.g. `d5w` deletes 5 words_
`D` | _delete the remainder of the line, starting with current cursor position_
`dd` | _delete the entire current line_
`Ndd` or `dNd` | _delete N lines, beginning with the current line e.g. `5dd` deletes 5 lines_

#### copy paste
Command | Description
-|-
`yy` | _copy the current line into the buffer_
`Nyy` or `yNy` | _copy the next N lines, including the current line, into the buffer_
`p` | _paste the line(s) in the buffer into the text after the current line_

## References
https://developer.ibm.com/technologies/systems/tutorials/au-customize_vi/
