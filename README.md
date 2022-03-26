## [GitSamples-GIT](../../tree/master): Create diff for AB with A


### prepare
    git checkout A
    git checkout -b "diff-AB-A"
    git rebase B

We see now the two files A and B with the history

    git log --oneline    

result:

    f01a47d A: init
    581b552 B: init
    e97f76f master: init

### diff
The current patch is **diff-AB-A**:

    git diff 581b552

Its content is:

    diff --git a/fileA b/fileA
    new file mode 100644
    index 0000000..8c7e5a6
    --- /dev/null
    +++ b/fileA
    @@ -0,0 +1 @@
    +A
    \ No newline at end of file

### diff for Files
After a commit we can check the README.md file now in the commit.

     git diff HEAD~1 README.md

show the following differences

    diff --git a/README.md b/README.md
    new file mode 100644
    index 0000000..4eaf7c3
    --- /dev/null
    +++ b/README.md
    @@ -0,0 +1,60 @@
    +## [GitSamples-GIT](../../tree/master): Create diff for AB with A
    +
    +
    ....


### Related Branches
* [patch-format-AB-patchA](../../tree/patch-format-AB-patchA)

### Links
* https://git-scm.com/docs/diff
* https://learntutorials.net/de/git/topic/273/git-diff
* https://stackoverflow.com/questions/10039747/how-to-view-file-diff-in-git-before-commit
