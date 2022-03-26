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

    git -am 0001-A-init.patch

It return just one line:

    Wende an: A: init

The history is not so nice,

    log --oneline

since we have our readme commit: But the we have our file again in the branch.

    2bbf142 A: init
    d0cb463 Adopt 0001-A-init.patch
    8120307 B: init
    e97f76f master: init

### Related Branches
* [patchA](../../tree/patchA)
* [patchB](../../tree/patchB)
* [patchAB](../../tree/patchAB)

### Links
* https://git-scm.com/docs/git-format-patch
* https://git-scm.com/docs/git-am
* https://mijingo.com/blog/creating-and-applying-patch-files-in-git
* https://www.tutorialspoint.com/git/git_patch_operation.htm
