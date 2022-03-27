## [GitSamples-GIT](../../tree/master): Github Links

Links to directories in README.md files not working as expected on github. 
The reason that all files are stored beneath the base path **blob**, 
    
    blob/<branch>/<path>/<fileName>

whereas directories are store beneath the base path **tree**:

    tree/<branch>/<path>


* Relative directory links not using parent navigation ".." works, since Github translate "magically": [dir](dir)
  * https://github.com/fluentcodes/GitSamples-GIT/blob/github-readme-links/dir to 
  * https://github.com/fluentcodes/GitSamples-GIT/tree/github-readme-links/dir.
* **Relative links to a parent directory does not work!**. One has write a link including **branch** for it. This is very nasty, since every link to a parent directory is broken when renaming or branching!
* A "dot" works in sub directories, but not branch root README.md.


### Directories Navigation
To create a link to the actual directory in the README.md file one has to use a link including the branch.
* [/../../tree/master](/../../tree/master): To master
* [/../../tree/github-readme-links](/../../tree/github-readme-links): this directory as branch root. "dot" does not work.
* [dir](dir): sub directory
* [dir/subdir](subdir): sub sub directory


### Samples
#### Files
All file entries starts with a **blob** in the path. So there are no problems linking to files from a README.md documentation.

| Link | works | Remarks |
| --- | --- | --- |
| [fileRoot](fileRoot) | ok | |
| [/fileRoot](/fileRoot) | ok | |
| [../github-readme-links/fileRoot](../github-readme-links/fileRoot)| ok |  include branch name|
| [../../blob/github-readme-links/fileRoot](../../blob/github-readme-links/fileRoot) | ok |  |
| [/../../blob/github-readme-links/fileRoot](/../../blob/github-readme-links/fileRoot) | ok |  |
| [GitSamples-GIT/blob/github-readme-links/fileRoot](GitSamples-GIT/blob/github-readme-links/fileRoot) | nok | Proposed in stackoverflow |
| [blob/github-readme-links/fileRoot](blob/github-readme-links/fileRoot) | nok | |
| [github-readme-links/fileRoot](github-readme-links/fileRoot)| nok |   |
| [/github-readme-links/fileRoot](/github-readme-links/fileRoot)| nok |  |
| | |
| [dir/fileDir](dir/fileDir) | ok | |
| [dir/subdir/README.md](dir/subdir/README.md) | ok |


#### Directories
All directory entries starts with **tree**, all README.md files with **blob**. Some type of links 
will magically replaced. 

| Link | Works | Remarks |
| --- | --- | --- |
| [dir](dir) | ok | automatic replacement **blob** by **tree** |
| [/dir](/dir) | ok | automatic replacement **blob** by **tree** |
| [../github-readme-links/dir](../github-readme-links/dir) | ok | automatic replacement **blob** by **tree** |
| [../../tree/github-readme-links/dir](../../tree/github-readme-links/dir) | ok | change from **blob** to **tree** |
| [/../../tree/github-readme-links/dir](/../../tree/github-readme-links/dir) | ok | change from **blob** to **tree** |
| [GitSamples-GIT/tree/github-readme-links/dir](GitSamples-GIT/tree/github-readme-links/dir) | nok | Proposed in stackoverflow |
| [tree/github-readme-links/dir](tree/github-readme-links/dir) | nok |  |
| [github-readme-links/dir](github-readme-links/dir) | nok |  |
| [/github-readme-links/dir](/github-readme-links/dir) | nok | |
|  |  |
| [/](/) | nok | points to the non-existing target https://github.com/fluentcodes/GitSamples-GIT/**blob**/github-readme-links |
| [.](.) | nok | points to the non-existing target https://github.com/fluentcodes/GitSamples-GIT/**blob**/github-readme-links |
| [..](..) | nok | points to the non-existing target https://github.com/fluentcodes/GitSamples-GIT/**blob** |
| [dir/subDir](dir/subdir) | ok | automatic replacement **blob** by **tree** |
| [../tree/master](../tree/master) | nok | 
| [../../tree/master](../../tree/master) | ok | Switching to branch. 
| [/../../tree/master](/../../tree/master) | ok | Switching to branch.

### Links
* https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
* https://stackoverflow.com/questions/7653483/github-relative-link-in-markdown-file