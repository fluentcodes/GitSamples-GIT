## [GitSamples-GIT](../../tree/master): Apply Patch File to patchB


### prepare
    git checkout patchB
    git checkout -b "patch-apply-B-patchA"

We see now the fileB with the history

    git log --oneline    

result:

    581b552 B: init
    e97f76f master: init


### patch
To apply the patch to the current branch, we use git am and pass in the name of the patch we want to apply.

    git am 0001-A-init.patch

It return just one line:

    Applying: A: init

The history is not so nice,

    log --oneline

since we have our readme commit: But the we have our file again in the branch.

    5ae1720 A: init
    c87a678 patch-apply-B-patchA
    581b552 B: init
    e97f76f master: init

### Related Branches
* [patch-format-AB-patchA](../../tree/patch-format-AB-patchA)

### Links
* https://git-scm.com/docs/git-format-patch
* https://git-scm.com/docs/git-am
* https://mijingo.com/blog/creating-and-applying-patch-files-in-git
* https://www.tutorialspoint.com/git/git_patch_operation.htm
