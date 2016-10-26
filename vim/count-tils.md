# Count TIL's

Count number of TIL's in til project.

Add below lines to ~/.vimrc.  
This allows .vimrc in each directories even if it does unsafe things.

```vim
set exrc
set secure
```

---

.vimrc in til project  
```vim
function! CountTils()
  execute '%s/^- \[//n'
endfunction

nnoremap <leader>c :call CountTils()<cr>
```

When you open README.md, press '\ + c'.  
This will read number of items with '- [link](#Reference)' format.  
It will show 'N matches on N lines' in terminal.

##### Reference

- [usage](https://github.com/jbranchaud/til#usage)
- [source](https://github.com/jbranchaud/til/blob/master/.vimrc)
