### [GitSamples-GIT](../../tree/master): Merge B into A

#### prepare
    git checkout A
    git checkout -b "merge-1B-into-1A"

#### merge 

    git merge 1B

    automatischer Merge von file
    KONFLIKT (hinzufügen/hinzufügen): Merge-Konflikt in file
    Automatischer Merge fehlgeschlagen; beheben Sie die Konflikte und committen Sie dann das Ergebnis.

#### file content

    <<<<<<< HEAD
    A
    =======
    B
    >>>>>>> 1B

#### log

    git log --oneline

output:

    8b8b176 (HEAD -> merge-1B-into-1A) merge-1B-into-1A: init
    c937225 (1B) 1B: init
    3740c5c (1A) 1A: init
    a8b83f8 (master) master: init

#### Related Branches
* [merge-1B_1A-into-1A](../../tree/merge-1B_1A_1A-into-1A)