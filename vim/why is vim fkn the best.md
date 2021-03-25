- no ceiling
- built primarily for editing - writing plain characters is secondary


## Syntax of the Vim Language
### Verb + Noun
#### Example
**d** for delete,
**w** for word
combine to "delete word"

### Verbs in Vim
The operation you want to take on the text
- `d` => **Delete**
- `c` => **Change** (delete and enter insert mode)
- `>` => **Indent**
- `v` => **Visually select**
- `y` => **Yank** (copy)

### Nouns in Vim (Motions)
- `w` => **word** (forward by a word)
- `b` => **back** (back by a word)
- `2j` => down 2 lines

### Nouns in Vim (Text Objects)
- `iw` => "inner word" (works from anywhere in a word)
- `it` => "inner tag" (the contents of an HTML tag)
- `i"` => "inner quotes"
- `ip` => "inner paragraph"
- `as` => "a sentence"

### Nouns in Vim (Parametrized Text Objects)
- `fx` / `Fx` => **forward**/**back** to (and including) char `x`
- `tx` / `Tx` => **forward**/**back** to (but **not** including) char `x`
- `/str` / `?str` => search next/previous "str"

## References
https://benmccormick.org/2014/07/02/learning-vim-in-2014-vim-as-language
https://www.youtube.com/watch?v=wlR5gYd6um0&ab_channel=thoughtbot
https://blog.carbonfive.com/vim-text-objects-the-definitive-guide/
https://medium.com/@mkozlows/why-atom-cant-replace-vim-433852f4b4d1
https://medium.com/usevim/stop-the-vim-configuration-madness-c825578bbf3e
https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim
