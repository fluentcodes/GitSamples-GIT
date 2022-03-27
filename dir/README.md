## [GitSamples-GIT](/../../tree/master): Readme in dir

### Directory Navigation 
The dot for self referencing directory in README.md works.
* [/../../tree/master](/../../tree/master): To master
* [/../../tree/github-readme-links](/../../tree/github-readme-links): Branch root
* [.](.): this directory
* [subdir](subdir): subdir


### Samples
#### Files
All file entries starts with a **blob** in the path. So there are no problems linking to files from a README.md documentation.

| Link | works | Remarks |
| --- | --- | --- |
| [fileDir](fileDir) | ok | Link zu local file |
| [/fileDir](/fileDir) | nok | Search fileDir in branch root     |
| [../../../blob/github-readme-links/dir/fileDir](../../../blob/github-readme-links/dir/fileDir) | ok |  |
| [/../../blob/github-readme-links/dirfileDir](/../../blob/github-readme-links/dir/fileDir) | ok |  |
| [../fileRoot](../fileRoot) | ok | |
| [subdir/README.md](subdir/README.md) | ok |


#### Directories
All directory entries starts with **tree**, all README.md files with **blob**. Some type of links
will magically replaced.

| Link | Works | Remarks |
| --- | --- | --- |
| [.](.) | ok | automatic replacement **blob** by **tree** |
| [../../github-readme-links/dir](../../github-readme-links/dir) | ok | automatic replacement **blob** by **tree** |
| [../../../tree/github-readme-links/dir](../../../tree/github-readme-links/dir) | ok | change from **blob** to **tree** |
| [/../../tree/github-readme-links/dir](/../../tree/github-readme-links/dir) | ok | Independent of README.md location|
|  |  |
| [/](/) | nok | points to the non-existing target https://github.com/fluentcodes/GitSamples-GIT/**blob**/github-readme-links |
| [.](.) | ok | self referencing |
| [..](..) | nok | points to the non-existing target https://github.com/fluentcodes/GitSamples-GIT/**blob**/github-readme-links |
| [subDir](subdir) | ok | |
| [/subDir](/subdir) | nok | |
| [/dir](/dir) | ok | |
| [../tree/master](../tree/master) | nok | Switching to branch.
| [../../../tree/master](../../../tree/master) | ok | Switching to branch.
| [/../../tree/master](/../../tree/master) | ok | Switching to branch.
