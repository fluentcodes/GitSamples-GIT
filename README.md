## [GitSamples-GIT](../../tree/master) switch --orphan: cherry-pick

As described in [switch-orphan-readme](../../tree/switch-orphan-readme) we want to put 
an orphan branch [_readme](../../tree/_readme) on the top of the history
to accomplish the work with topic branches.

#### Preparation

Now preparing a topic branch to add README.md template at the end:

    git checkout _empty
    git checkout -b "switch-orphan-readme-cherry-pick"
    echo "" >> .gitignore;
    git add .
    git commit -m "switch-orphan-readme-cherry-pick"

##### Files

    git ls-files

    .gitignore

##### History:

    git log --oneline

    0d86dce (HEAD -> switch-orphan-empty-branch) switch-orphan-empty-branch:init
    4767389 (origin/_empty, _empty) empty:init    4767389 (HEAD -> switch-orphan-empty-branch, origin/_empty, _empty) empty:init

### Add README.md
Using cherry-pick we need the hash id of the orphan [_readme](../../tree/_readme)

    git log --oneline _readme

    4bcfbe3 (origin/_readme, _readme) _readme:init


The hash of [_readme](../../tree/_readme) is **4bcfbe34**. 

    git cherry-pick 4bcfbe34

#### History
Now we have the orphan [_readme](../../tree/_readme) branch containing README.md 
at the top. 

    git log --oneline

    441aadc (HEAD -> switch-orphan-readme-cherry-pick) _readme:init
    c0d322b switch-orphan-readme-cherry-pick:init
    4767389 (origin/_empty, _empty) empty:init

#### Files

    git ls-files

    .gitignore
    README.md

### Related Branches
* [switch-orphan](../../tree/switch-orphan)
* [switch-orphan-readme](../../tree/switch-orphan-readme)
* [switch-orphan-readme-rebase](../../tree/switch-orphan-readme-rebase)
* [switch-orphan-readme-merge](../../tree/switch-orphan-readme-merge)
* [_empty](../../tree/_empty)
* [_readme](../../tree/_readme)
* [readme](../../tree/readme)

### Links
* https://git-scm.com/docs/git-switch
* https://stackoverflow.com/questions/34100048/create-empty-branch-on-github
* https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo