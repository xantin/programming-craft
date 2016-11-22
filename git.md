# GIT

## Find commit where file was added
`git log --diff-filter=A -- name_of_file`
e.i. `git log --diff-filter=A -- foo.js`

types of files:
* A: addition of a file
* C: copy of a file into a new one
* D: deletion of a file
* M: modification of the contents or mode of a file
* R: renaming of a file
* T: change in the type of the file
* U: file is unmerged (you must complete the merge before it can be committed)
* X: "unknown" change type (most probably a bug, please report it)
