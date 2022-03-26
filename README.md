### [GitSamples-GIT](../../tree/master): Cherrypick D from FEDCBA onto A

Here we will pick branch **D** from branch **FEDCBA**

#### prepare
    git checkout A
    git checkout -b "cherrypick-FEDCBA-D-onto-A"

#### find the appropriate commit

    git checkout rebase-FEDCBA

With

    git log --oneline

we can select D

    57c28b5 rebase-FEDCBA:init
    1108090 F:init
    2d9b7ed E:init
    0ded26b D: init
    e279f55 C: init
    d6c1fbe B: init
    5048e61 A: init
    e97f76f master: init

with a has of 0ded26b
#### Related Branches
* [rebase-FEDCBA](../../tree/rebase-DCBA)

#### Links 
* https://git-scm.com/docs/git-cherry-pick