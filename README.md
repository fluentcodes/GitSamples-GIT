## [GitSamples-GIT](../../tree/master): Automate GIT
It could be rather boring to type some complicated git commands one use several times a day. 
And some of the parameters are rather unintuitive for e.g. 

     git add .

which uses a "." instead of everydays "*".

Purpose of this topic branch is to develop and describe a number of everydays helper. 

## aliases
All aliases starts with "g".

    alias ga='git add .;'
    alias gaca='ga; git commit --amend'
    alias gacan='gaca --no-edit;'
    alias gacap='gacan git push -f'
    alias gca='git commit --amend'
    alias glo='git log --oneline'
    alias gs='git status'

### For Fun
* alias lol='git log --oneline'

### Links
* https://medium.com/@RebyOliveira/automate-your-github-using-shell-script-570a97844dc0
* https://opensource.com/article/20/1/bash-scripts-git
* https://wiki.ubuntuusers.de/alias/