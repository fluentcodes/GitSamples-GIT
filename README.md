### [GitSamples-GIT](../../tree/master): Rebase 1A onto 1

#### prepare
    git checkout 1A
    git checkout -b "rebase-1A-onto-1B"

#### rebase 

    git rebase 1B

    automatischer Merge von file
    KONFLIKT (hinzufügen/hinzufügen): Merge-Konflikt in file
    error: Konnte db82225... (1A: init) nicht anwenden
    Hinweis: Resolve all conflicts manually, mark them as resolved with
    Hinweis: "git add/rm <conflicted_files>", then run "git rebase --continue".
    Hinweis: You can instead skip this commit: run "git rebase --skip".
    Hinweis: To abort and get back to the state before "git rebase", run "git rebase --abort".
    Konnte db82225... (1A: init) nicht anwenden

#### file content

    <<<<<<< HEAD
    B
    =======
    A
    >>>>>>> db82225 (1A: init)

#### log

    git log --oneline

output:

    8b8b176 (HEAD -> merge-1B-into-1A) merge-1B-into-1A: init
    c937225 (1B) 1B: init
    3740c5c (1A) 1A: init
    a8b83f8 (master) master: init

#### status
    Nicht zusammengeführte Pfade:
    (benutzen Sie "git restore --staged <Datei>..." zum Entfernen aus der Staging-Area)
    (benutzen Sie "git add/rm <Datei>...", um die Auflösung zu markieren)
    von beiden hinzugefügt: file

#### Related Branches
* [merge-1B-into-1A](../../tree/merge-1B-into-1A)