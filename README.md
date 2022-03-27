## [GitSamples-GIT](../../tree/master): switch --orphan
With 

    git switch --orphan branchname

one can create branches in the repository without history. 

For [GitSamples-GIT](../../tree/master) the following orphan branches are used:
* [_empty](../../tree/_empty): Contains .gitignore
* [_readme](../../tree/_readme) commit Contains README.md template without history

To find the best way to use the orphan [_readme](../../tree/_readme) 
branch there is a separate [switch-orphan-readme](../../tree/switch-orphan-readme) branch which describe different possibilities. 

The used branches are created like this:    

    git switch --orphan _empty
    // .... add .gitignore and commit

#### History

    git log --oneline    

    4767389 (HEAD -> _empty, origin/_empty) empty:init

### Related Branches
* [switch-orphan-readme](../../tree/switch-orphan-readme)
* [switch-orphan-readme](../../tree/switch-orphan-cherry-pick)
* [switch-orphan-readme-rebase](../../tree/switch-orphan-readme-rebase)
* [switch-orphan-readme-merge](../../tree/switch-orphan-readme-merge)
* [_empty](../../tree/_empty)
* [_readme](../../tree/_readme)
* [readme](../../tree/readme)

### Links
* https://git-scm.com/docs/git-switch
* https://stackoverflow.com/questions/34100048/create-empty-branch-on-github
* https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo