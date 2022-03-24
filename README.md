### [GitSamples-GIT](../../tree/master): Rebase 1B_1A onto 1A
Here we have the commit **db82225** in the history of 1B_1A. So an automatic merge could be done
different than [rebase-1A-1B](../../tree/rebase-1A-1B).

The content of **file** will be B.

#### prepare
    git checkout 1B_1A
    git checkout -b "rebase-1B_1A-onto-1A"

#### rebase 

    git rebase 1A

    warning: skipped previously applied commit 3740c5c
    hint: use --reapply-cherry-picks to include skipped commits
    hint: Disable this message with "git config advice.skippedCherryPicks false"
    Successfully rebased and updated refs/heads/rebase-1B_1A-onto-1A.

#### file content

    B

#### log

    git log --oneline

output:

    4a1f46b (HEAD -> rebase-1B_1A-onto-1A) 1B: init
    db82225 (origin/1A, 1A) 1A: init
    a8b83f8 master: init


#### Related Branches
* [merge-1B_1A-into-1A](../../tree/merge-1B_1A-into-1A)
* [rebase-1A-1B](../../tree/rebase-1A-1B)

#### Links 
* https://git-scm.com/docs/git-rebase