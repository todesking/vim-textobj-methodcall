# vim-textobj-methodcall

```
Map[Integer]
foo(1, 2, 3)
    ~~ic~~~
~~~~~ac~~~~~
```


## Requirements

* [vim-textobj-user](https://github.com/kana/vim-textobj-user)
* [vim-operator-surround](https://github.com/rhysd/vim-operator-surround)(optional)

## Settings

```vim
" Optional: override keys. default: 'ac', 'ic'
let g:textobj#methodcall#select_a = 'ac'
let g:textobj#methodcall#select_i = 'ic'

" Optional: set word pattern for specific filetype
call textobj#methodcall#register_word_pattern('r', '\v[a-zA-Z0-9_.]+')

" Required(if operator-surround used): operator-surround settings
let g:operator#surround#blocks =
    \ textobj#methodcall#operator_surround_blocks(deepcopy(g:operator#surround#default_blocks), 'c')
```

## Related plugins

* [argtextobj.vim](http://www.vim.org/scripts/script.php?script_id=2699)
  * textobj for argument
