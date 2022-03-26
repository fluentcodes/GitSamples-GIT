## GitSamples-GIT Topic Branch: master

The topic branches you find in this GitSamples repository contains some hands on examples for simple git operations.

It shows the concept of GitSamples: Using git branches not only temporarily but as permanent space for scenarios with 
working examples in a certain environment with markdown documentation as a space to document, contribute and share.

### Gitsample Evaluations
* [automate-Git](/../../tree/automate-git): Aliases for simplify git shell work.
* [github-readme-links](/../../tree/github-readme-links): The strange behaviour of markdown links in Github.
* [switch-orphan-readme](/../../tree/switch-orphan-readme): Some investigation to create new topic branches with a "clean" history.


### Merge
* [merge-1B-into-1A](../../tree/merge-1B-into-1A): A merge from branch 1B into 1A with conflicts.
* [merge-1B_1A-into-1A](../../tree/merge-1B_1A-into-1A): A merge from branch 1B into 1A with no conflicts since 1A is in history.

### Rebase
* [rebase-DCBA](../../tree/rebase-DCBA): How [DCBA](../../tree/DCBA) is created.
* [rebase-FE](../../tree/rebase-FE): How [FE](../../tree/FE) is created.
* [rebase-FEDCBA](../../tree/rebase-FEDCBA): How [FEDCBA](../../tree/FEDCBA) is created.
* [rebase-1B_1A-onto-1A](../../tree/rebase-1B_1A-onto-1A):
* [rebase-interactive-FEDCBA-squashto-BA](../../tree/rebase-interactive-FEDCBA-squashto-BA): interactiv with squash.


### Patch
* [patch-format-AB-patchA](../../tree/patch-format-AB-patchA): Create a patch
* [patch-apply-B-patchA](../../tree/patch-apply-B-patchA): Apply the previous patch


### Others
There are several branches for other git operations. The following ones has a more 
* [cherrypick-FEDCBA-D-onto-A](../../tree/cherrypick-FEDCBA-D-onto-A): A cherry-pick example
* [diff-AB-A](../../tree/diff-AB-A): A diff example

### Branches with files
These branches contains one file containing simple characters which are used for the git samples in Topic Branches.

#### File for Conflict Scenarios
These branches contains only the file "file"
* [1A](../../tree/1A): File contains A in first line
* [1B](../../tree/1B): File contains B in first line
* [1B_1A](../../tree/1B_1A): File contains B with A in history

#### File without Conflict Scenarios
* [A](../../tree/A): Contains fileA with .gitignore
* [B](../../tree/B): Contains fileB with .gitignore
* [C](../../tree/C): Contains fileC with .gitignore
* [D](../../tree/D): Contains fileD with .gitignore
* [E](../../tree/E): Contains fileE with .gitignore
* [F](../../tree/F): Contains fileF with .gitignore

#### Several Files without Conflict Scenarios
* [DCBA](../../tree/DCBA): Contains fileA, fileB, fileC and fileD with .gitignore
* [FE](../../tree/FE): Contains fileF and fileE with .gitignore
* [FEDCBA](../../tree/FEDCBA): Contains fileA, fileB, fileC, fileD, fileE and fileF with .gitignore


