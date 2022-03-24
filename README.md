### [GitSamples-GIT](../../tree/master): Rebase 1A onto 1B

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

    0cea9e7 (HEAD -> rebase-1A-1B) 1A: init
    c937225 (origin/1B, 1B) 1B: init
    a8b83f8 master: init

#### status
    Nicht zusammengeführte Pfade:
    (benutzen Sie "git restore --staged <Datei>..." zum Entfernen aus der Staging-Area)
    (benutzen Sie "git add/rm <Datei>...", um die Auflösung zu markieren)
    von beiden hinzugefügt: file

#### resolve
Change the content of the file to A. 

     git add .
     git rebase --continute

    [losgelöster HEAD 0cea9e7] 1A: init
    1 file changed, 46 insertions(+)
    create mode 100644 README.md
    Erfolgreich Rebase ausgeführt und refs/heads/rebase-1A-1B aktualisiert.

#### Related Branches
* [merge-1B-into-1A](../../tree/merge-1B-into-1A)

#### Links 
* https://git-scm.com/docs/git-rebase
* https://apple.stackexchange.com/questions/337244/homebrew-and-git-wrong-language-on-the-command-line
* https://stackoverflow.com/questions/14189134/how-to-change-git-from-chinese-to-english-in-mac