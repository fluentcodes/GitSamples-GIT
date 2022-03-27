## [GitSamples-GIT](../../tree/master) switch --orphan: readme

I want examine if one could combine unrelated branches to create a topic branch
with a README.md template at the top.

The use case for example in the [FEDCBA](../../tree/FEDCBA) branch we rebase only other branches containing files. At the 
end this should be documented in a README.md file on [rebase-FEDCBA](../../tree/rebase-FEDCBA).

If its possible to add a readme template branch on top of the history, 
this could simplify the documentation in topic branches.

### Prepare

#### Orphan Branches
For this I created three branches.
* [_empty](../../tree/_empty): Contains .gitignore
* [_readme](../../tree/_readme) commit Contains README.md template without history
* [readme](../../tree/readme) commit Contains README.md template based on [_empty](../../tree/_empty)

The branches are created like this:    

    git switch --orphan _empty
    // .... add .gitignore and commit
    git switch --orphan _readme
    // .... add README.md template and commit#
    git checkout _readme
    git checkout -b "readme"
    git rebase _empty

The [readme](../../tree/readme) branch has now [_empty](../../tree/_empty) in history: 

    git log --oneline

    0af75cd (HEAD -> readme) _readme:init
    4767389 (origin/_empty, _empty) empty:init

### README.md branches

We have three different solutions described: 

* [switch-orphan-readme-cherry-pick](../../tree/switch-orphan-readme-cherry-pick): readme at the top.
* [switch-orphan-readme-rebase](../../tree/switch-orphan-readme-rebase): readme at the bottom.
* [switch-orphan-readme-merge](../../tree/switch-orphan-readme-merge): readme before bottem.



### Conclusion
With a [cherry-pick](../../tree/switch-orphan-readme-cherry-pick) one can combine orphan branches in the desired way. 

### Related Branches
* [switch-orphan](../../tree/switch-orphan)
* [switch-orphan-readme-cherry-pick](../../tree/switch-orphan-readme-cherry-pick)
* [switch-orphan-readme-rebase](../../tree/switch-orphan-readme-rebase)
* [switch-orphan-readme-merge](../../tree/switch-orphan-readme-merge)
* [_empty](../../tree/_empty)
* [_readme](../../tree/_readme)
* [readme](../../tree/readme)

### Links
* https://git-scm.com/docs/git-switch
* https://stackoverflow.com/questions/34100048/create-empty-branch-on-github
* https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo