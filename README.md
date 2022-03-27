## [GitSamples-GIT](../../tree/master): Automate GIT
It could be rather boring to type some complicated git commands one use several times a day. 
And some of the parameters are rather unintuitive for e.g. 

     git add .

which uses a "." instead of everydays "*".

Purpose of this topic branch is to develop and describe a number of everydays helper. 

## Aliases
All aliases starts with "g".

    alias ga='git add .;'
    alias gaca='ga; git commit --amend'
    alias gacan='gaca --no-edit;'
    alias gacap='gacan git push -f'
    alias gb='git branch'
    alias gba='gb --all'
    alias gca='git commit --amend'
    alias glo='git log --oneline'
    alias gs='git status'

## Methods

### new
The following function alias cereats a new branch from [_empty](../../tree/_empty) with **INPUT** as name and an 
initial commit "INPUT:init".

    alias new='function _new(){git checkout _empty; git checkout -b "$1"; echo "" >> .gitignore; ga; git commit -m "$1:init"};_new'

##### Example

    new test

    Switched to branch '_empty'
    Your branch is up to date with 'origin/_empty'.
    Switched to a new branch 'test'
    [test d5856b5] test:init
    1 file changed, 1 insertion(+)
    
##### Logs

    d5856b5 (HEAD -> test) test:init
    4767389 (origin/_empty, _empty) empty:init

### For Fun
* alias lol='git log --oneline'

### Links
* https://unix.stackexchange.com/questions/31947/how-to-add-a-newline-to-the-end-of-a-file
* https://medium.com/@RebyOliveira/automate-your-github-using-shell-script-570a97844dc0
* https://opensource.com/article/20/1/bash-scripts-git
* https://wiki.ubuntuusers.de/alias/
* https://stackoverflow.com/questions/941338/how-to-pass-command-line-arguments-to-a-shell-alias