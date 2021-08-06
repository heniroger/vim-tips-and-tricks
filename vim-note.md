# Vim note

## Vim Plugin
```yml
Vundle
Prettier
NerdTree
Vdebug
vim-gitgutter # show line you add in git
Vim Fugitive # git
Fzf vim # file finder
Tagbar
Ctag

Vim surround :(
Syntastic
vim ctrlp
vim airline # this is the bad alternative of powerline

```
## CTags PHP Command
```bash
# dependencies tags file (index only the vendor directory, and save tags in ./tags.vendors)
$ ctags -R --PHP-kinds=cfi -f tags.vendors vendor

# project tags file (index only src, and save tags in ./tags; AutoTags will update this one)
$ ctags -R --PHP-kinds=cfi src
```
