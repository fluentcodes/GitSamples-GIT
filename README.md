### [GitSamples-GIT](../../tree/master): Rebase 1B_1A onto 1B
Here we have a merge conflict different to [rebase-1B_1A-1A](../../tree/rebase-1B_1A-1A.

This is due we have 
* 1B: first commit file is B
* 1A: conflict file is now A
* 1B: conflict file is now B

#### prepare
    git checkout 1B_1A
    git checkout -b "rebase-1B_1A-onto-1B"

#### rebase 

    Auto-merging file
    CONFLICT (add/add): Merge conflict in file
    error: could not apply 3740c5c... 1A: init
    hint: Resolve all conflicts manually, mark them as resolved with
    hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
    hint: You can instead skip this commit: run "git rebase --skip".
    hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
    Could not apply 3740c5c... 1A: init

#### file content

    <<<<<<< HEAD
    B
    =======
    A
    >>>>>>> 3740c5c (1A: init)

#### log

    git log --oneline

output:

    c937225 (HEAD, origin/1B, 1B) 1B: init
    a8b83f8 master: init


#### resolve
We have to rebase several times since we start with 
* 1B with B
* overwrite with 1A
* overwrite with 1B.

This happens in real live if one rebase several commit with conflict.

So we have tree times
* resolve conflict
* git add .
* git rebase --continue


Finally: 
    
    [detached HEAD ef131ff] 1B: init
    1 file changed, 1 insertion(+), 2 deletions(-)
    Successfully rebased and updated refs/heads/rebase-1B_1A-onto-1B.

#### final history

    git log --oneline

resulting

    ef131ff (HEAD -> rebase-1B_1A-onto-1B) 1B: init
    50605c7 1B: init
    312c239 1A: init
    c937225 (origin/1B, 1B) 1B: init
    a8b83f8 master: init


#### Related Branches
* [merge-1B_1A-into-1A](../../tree/merge-1B_1A-into-1A)
* [merge-1B_1A-into-1A](../../tree/rebase-1B_1A-into-1A)
* [rebase-1A-1B](../../tree/rebase-1A-1B)

#### Links 
* https://git-scm.com/docs/git-rebase