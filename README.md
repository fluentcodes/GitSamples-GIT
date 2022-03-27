## [GitSamples-GIT](../../tree/master): branch

    git branch

     1A
    1A2B
    1B
    ...

### Upstream

    git branch --unset-upstream

### Filter for names
    git branch --list '*orphan*'

    switch-orphan
    switch-orphan-readme
    switch-orphan-readme-cherry-pick
    switch-orphan-readme-merge
    switch-orphan-readme-rebase

#### Shell Alias
    alias gbl='function _gbl(){git branch --list "*$1*"};_gbl'

With this alias in the profile the call simplifies to 

    gbl orphan

    switch-orphan
    switch-orphan-readme
    ...

### Links
* https://git-scm.com/docs/git-branch
* https://devconnected.com/how-to-set-upstream-branch-on-git/
* https://stackoverflow.com/questions/31787803/how-do-i-search-for-branch-names-in-git