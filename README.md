### [GitSamples-GIT](../../tree/master): Rebase FE
Here we do one rebase commands to merge the branch **F** to branch **E** the branches **FE**.  
Since the content of each branch is a separate file
F and E there are no conflicts.

#### prepare
    git checkout F
    git checkout -b "rebase-FE"

#### rebase 

    git rebase E

with feedback

    Zunächst wird der Branch zurückgespult, um Ihre Änderungen
    darauf neu anzuwenden ...
    Wende an: F:init
    Verwende Informationen aus der Staging-Area, um ein Basisverzeichnis nachzustellen ...
    A       README.md
    Falle zurück zum Patchen der Basis und zum 3-Wege-Merge ...

#### result

We have the two files in one branch.
* fileE
* fileF

#### log

    git log --oneline

output:

    bc5fff3 F:init
    2b11417 E:init
    e97f76f master: init

#### Related Branches
* [rebase-DCBA](../../tree/rebase-DCBA)
* [rebase-FEDCBA](../../tree/rebase-FEDCBA)

#### Links 
* https://git-scm.com/docs/git-rebase