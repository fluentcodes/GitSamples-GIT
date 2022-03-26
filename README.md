### [GitSamples-GIT](../../tree/master): Rebase FEDCBA

Here we have one rebase command for the branch **FE** onto branch **DCBA**.  
Since the content of each branch is a separate file
F, E, D, C, B and A with no conflicts.

#### prepare
    git checkout FE
    git checkout -b "rebase-FEDCBA"

#### rebase 

    git rebase DCBA

The feedback as followed:

    First, rewinding head to replay your work on top of it...
    Applying: Rebase DCBA:init
    Applying: E:init
    Applying: F:init

#### result

Now e have the six files in one branch.

* fileA
* fileB
* fileC
* fileD
* fileE
* fileF

#### log

    git log --oneline

output:

    1e53516 F: init
    145a797 E:init
    04e22ca D: init
    8965b82 C: init
    5d5ab52 B: init
    6939312 A: init
    e97f76f master: init

#### Related Branches
* [rebase-DCBA](../../tree/rebase-DCBA)
* [rebase-FE](../../tree/rebase-FE)

#### Links 
* https://git-scm.com/docs/git-rebase