## [GitSamples-GIT](../../tree/master) switch --orphan: rebase

As described in [switch-orphan-readme](../../tree/switch-orphan-readme) we want to put 
an orphan branch [_readme](../../tree/_readme) on the top of the history
to accomplish the work with topic branches.

#### Preparation

Now preparing a topic branch to add README.md template at the end:

    git checkout _empty
    git checkout -b "switch-orphan-readme-rebase"
    echo "" >> .gitignore;
    git add .
    git commit -m "switch-orphan-readme-rebase"

##### Files

    git ls-files

    .gitignore

##### History:

    git log --oneline

    979aaa3 (HEAD -> switch-orphan-readme-rebase) switch-orphan-readme-rebase:init
    4667a53 (_empty) switch-orphan-readme-rebase:init
    4767389 (origin/_empty) empty:init

### Add README.md
We rebase our current branch with the orphan [_readme](../../tree/_readme).

    git rebase _readme

#### History
Now we have the orphan [_readme](../../tree/_readme) with the file README.md 
at the bottom. 

    git log --oneline

    7c4f816 (HEAD -> switch-orphan-readme-rebase) switch-orphan-readme-rebase:init
    2b1147e switch-orphan-readme-rebase:init
    f3c0f5c empty:init
    4bcfbe3 (origin/_readme, _readme) _readme:init

#### Files

    git ls-files

    .gitignore
    README.md

### Related Branches
* [switch-orphan](../../tree/switch-orphan)
* [switch-orphan-readme](../../tree/switch-orphan-readme)
* [switch-orphan-readme-cherry-pick](../../tree/switch-orphan-readme-cherry-pick)
* [switch-orphan-readme-merge](../../tree/switch-orphan-readme-merge)
* [_empty](../../tree/_empty)
* [_readme](../../tree/_readme)
* [readme](../../tree/readme)

### Links
* https://git-scm.com/docs/git-switch
* https://stackoverflow.com/questions/34100048/create-empty-branch-on-github
* https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo