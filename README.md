### [GitSamples-GIT](../../tree/master): Rebase DCBA
Here we do four rebase commands for the branches D, C, B, A. Since the content of each branch is a separate file
D, C, B, A there are no conflicts.

#### prepare
    git checkout D
    git checkout -b "rebase-DCBA"

#### rebase 

    git rebase C
    git rebase B
    git rebase A

Foreach command you will same feedback. For the last one it is

    First, rewinding head to replay your work on top of it...
    Applying: B: init
    Using index info to reconstruct a base tree...
    A       README.md
    Falling back to patching base and 3-way merge...
    Applying: C: init
    Applying: D: init

#### result

We have the four files in one branch.
* fileA
* fileB
* fileC
* fileD

#### log

    git log --oneline

output:

    244632f D: init
    f117cc8 C: init
    91679b9 B: init
    6939312 A: init
    e97f76f master: init

#### Related Branches
* [rebase-FE](../../tree/rebase-FE)
* [rebase-FEDCBA](../../tree/rebase-FEDCBA)

#### Links 
* https://git-scm.com/docs/git-rebase