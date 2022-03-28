## [GitSamples-GIT](../../tree/master) switch --orphan: merge

As described in [switch-orphan-readme](../../tree/switch-orphan-readme) we want to put 
an orphan branch [_readme](../../tree/_readme) on the top of the history
to accomplish the work with topic branches.

#### Preparation

Now preparing a topic branch to add README.md template at the end:

    git checkout _empty
    git checkout -b "switch-orphan-readme-merge"
    echo "" >> .gitignore;
    git add .
    git commit -m "switch-orphan-readme-merge"

##### Files

    git ls-files

    .gitignore

##### History:

    git log --oneline

    0d86dce (HEAD -> switch-orphan-empty-branch) switch-orphan-empty-branch:init
    4767389 (origin/_empty, _empty) empty:init    4767389 (HEAD -> switch-orphan-empty-branch, origin/_empty, _empty) empty:init

### Add README.md
We merge our prepared  [readme](../../tree/readme) branch with [_empty](../../tree/_empty) in history.

    git merge readme

#### History
Now we have the orphan [_readme](../../tree/_readme) branch containing README.md 
a third place. 

    git log --oneline

    adfcc3b (HEAD -> switch-orphan-readme-merge) Merge branch 'readme' into switch-orphan-readme-merge
    e39eb8c switch-orphan-readme-merge:init
    0af75cd (origin/readme, readme) _readme:init
    4767389 (origin/_empty) empty:init


#### Files

    git ls-files

    .gitignore
    README.md

### Related Branches
* [switch-orphan](../../tree/switch-orphan)
* [switch-orphan-readme](../../tree/switch-orphan-readme)
* [switch-orphan-readme-rebase](../../tree/switch-orphan-readme-rebase)
* [switch-orphan-readme-cherry-pick](../../tree/switch-orphan-readme-cherry-pick)
* [_empty](../../tree/_empty)
* [_readme](../../tree/_readme)
* [readme](../../tree/readme)

### Links
* https://git-scm.com/docs/git-switch
* https://stackoverflow.com/questions/34100048/create-empty-branch-on-github
* https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo