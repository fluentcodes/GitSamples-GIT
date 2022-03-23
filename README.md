### [GitSamples-GIT](../../tree/master): Merge B_A into A

#### prepare
    git checkout A
    git checkout -b "merge-1B_1A-into-1A"

#### merge

    git merge 1B_1A

This will result the content B for **file** without conflicts since A is part of the history.

#### file content

    B

#### log

    git log --oneline

output:

    1537ff4 (HEAD -> merge-1B_1A-into-1A, origin/merge-1B_1A-into-1A) merge-1B:1A-into-1A
    06d1f87 (origin/1B_1A, 1B_1A) 1B: init
    3740c5c (origin/1A, 1A) 1A: init
    a8b83f8 (origin/master, master) master: init

#### Related Branches
* [merge-1B_1A-into-1A](../../tree/merge-1B_1A-into-1A)