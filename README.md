### [GitSamples-GIT](../../tree/master): Rebase interactive with squash FEDCBA into BA

One can merge the last commits to simplify history. This will simplify rebasing/merge problems. If you rebase a changed file with conflicts,
the conflict has to be solved for each commit. This could be a rather annoying thing. So sqashing is an appropriate mean for
this.

Here we have one rebase interactitve command for the branch **FEDCBA**.  
Squashing the commits F, E, D, C into one "rebased interactive FEDCBA to BA".  
Since the content of each branch is a separate file
F, E, D, C, B and A there are no conflicts.

#### prepare
    git checkout FEDCBA
    git checkout -b "rebase-interactive-FEDCBA-squashto-BA"

#### log

    git log --oneline

results

    57c28b5 rebase-FEDCBA:init  
    1108090 F:init  
    2d9b7ed E:init  
    0ded26b D: init  
    e279f55 C: init d6c1fbe  
    B: init 5048e61 A: init  
    e97f76f master: init


#### rebase 

    git rebase -i HEAD~4

#### editor
An editor opens to fix the commits. Only the commits from the bottom line can be modified with squash:

    # Rebase d6c1fbe..499b8e7 onto d6c1fbe (5 commands)
    #
    # Commands:
    # p, pick = use commit
    
    pick e279f55 C: init
    pick 0ded26b D: init
    pick 2d9b7ed E:init
    pick 1108090 F:init
    
    # This is a combination of 5 commits.
    # This is the 1st commit message:
    C: init
    
    # This is the commit message #2:
    
    D: init
    
    # This is the commit message #3:
    
    E:init
    
    # This is the commit message #4:
    
    F:init
    
    # Please enter the commit message for your changes. Lines starting
    # with '#' will be ignored, and an empty message aborts the commit.


#### Modifiy
We repöace pick by squash or s:

    pick e279f55 C: init
    s 0ded26b D: init
    s 2d9b7ed E:init
    s 1108090 F:init
`

#### Fix last commit message

Wie will replace the commit message "C:init" by "rebased interactive FEDCBA to CBA"

    # This is a combination of 5 commits.
    # This is the 1st commit message:
    C: init
    
    # This is the commit message #2:
    
    D: init
    
    # This is the commit message #3:
    
    E:init
    
    # This is the commit message #4:
    
    F:init
    
    # This is the commit message #5:
    
    rebase-FEDCBA:init
    
    # Please enter the commit message for your changes. Lines starting
    # with '#' will be ignored, and an empty message aborts the commit.


#### Result

    6 files changed, 45 insertions(+)
    create mode 100644 .gitignore
    create mode 100644 C
    create mode 100644 D
    create mode 100644 E
    create mode 100644 F
    create mode 100644 README.md
    Successfully rebased and updated refs/heads/rebase-interactiv-FEDCBA-BA.

#### log

    git log --oneline

output:

679c34f rebased interactive FEDCBA to BA
d6c1fbe B: init
5048e61 A: init
e97f76f master: init

#### Related Branches
* [rebase-DCBA](../../tree/rebase-FEDCBA)

#### Links 
* https://git-scm.com/docs/git-rebase