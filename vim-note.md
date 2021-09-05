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

## CTags Shortcuts

- CTRL-N and CTRL-P : Auto complete
- CTRL-] : Auto Complete 

# Tmux shortcuts

Client or session : has one or multiple windows
Window :  has one or multiple  splited pane 
Pane : by default : default bash prompt in your terminal

- Leader : Ctrl-B

- Leader+W : Select prompt Tab or windows 
- Leader+d : Detach session
- Leader+D : Detach session : With Select prompt
- Leader+$ : Rename session
- Leader+) : Next session : switch client
- Leader+( : Preview session : switch client

- Leader+! : Break pane

- Leader+c : create new tab
- Leader+C : create session : new client

- Leader+" : split window horizontally
- Leader+% : split window 
- Leader+& : kill window
- Leader+x : kill Pane
- Leader+X : kill Session

- Leader+z : Resize pane to One (switch split)  



