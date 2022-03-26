## [GitSamples-GIT](../../tree/master): Create Patch File for A


### prepare
    git checkout A
    git checkout -b "patch-format-AB-patchA"
    git rebase patchB

We see now the two files A and B with the history

    git log --oneline    

result:

    2cb88ad A: init
    581b552 B: init
    e97f76f master: init

The difference between AB and B will now created

### patch
The current patch is **patch-format-AB-patchA**:

    git format-patch B

creating the file ** 0001-A-init.patch**.

Its content is:

    From 2cb88adbca339657df0b8d9df666edc56c3c809b Mon Sep 17 00:00:00 2001
    From: WerDiw <werner.diwischek@witt-gruppe.eu>
    Date: Thu, 24 Mar 2022 06:10:23 +0100
    Subject: [PATCH] A: init
    
    ---
     fileA | 1 +
     1 file changed, 1 insertion(+)
     create mode 100644 fileA
    
    diff --git a/fileA b/fileA
    new file mode 100644
    index 0000000..8c7e5a6
    --- /dev/null
    +++ b/fileA
    @@ -0,0 +1 @@
    +A
    \ No newline at end of file
    -- 
    2.11.0


### Related Branches
* [patch-apply-B-patchA](../../tree/patch-apply-B-patchA)

### Links
* https://git-scm.com/docs/git-format-patch
* https://git-scm.com/docs/git-am
* https://mijingo.com/blog/creating-and-applying-patch-files-in-git
* https://devconnected.com/how-to-create-and-apply-git-patch-files/
* https://www.tutorialspoint.com/git/git_patch_operation.htm
* https://docs.gitlab.com/omnibus/development/creating-patches.html
