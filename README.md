### [GitSamples-GIT](../../tree/master): Cherry-pick D from FEDCBA onto A

Here we will pick branch **D** from branch **FEDCBA** and add it to the branch A.

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

with a commit hash of "0ded26b"

#### cherry-pick

When applying the commit from FEDCBA

    git cherry-pick 0ded26b 

we have the file D into our branch. We could also use the full hash 0ded26b96a8edeac820f6d90682a666ac62e622d.

    git log --oneline

results

    546c971 D: init
    ac2bac9 cherrypick-FEDCBA-D-onto-A:init
    882f49d A: init
    e97f76f master: init


#### Related Branches
* [rebase-FEDCBA](../../tree/rebase-DCBA)

#### Links 
* https://git-scm.com/docs/git-cherry-pick
* https://mijingo.com/blog/using-git-cherry-pick
