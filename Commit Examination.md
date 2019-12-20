# How to examine different commits

There are different ways to examine the commits performed. 

1. **difference** One way is to look at the differece between two commits\
$ git diff 249309a2 7ecdf7f

Note: The 8-digit value is the 8 first digits of two SHA values assigned to two different commits. Each commit has a SHA value assigned to it, e.g. commit **7ecdf7ff**97b0c679be0e73169ba19bb56431b46e

2. **show** The other way is to look directly into the changes of each commit\
$ git show 249309a2


Note: The most recent commit is also named HEAD commit. So, it can also be called not only by its SHA value, but also by HEAD.\
$ git show HEAD

Note: For commits before the HEAD commit, we can alter the above code to go a few more past commits. For example for two commits before the HEAD commit, we can use:\
$ git show HEAD~2

Note: We can use git diff by using HEAD as below:\
$git diff HEAD~2 HEAD~4

3. **annotate** which allows to examine all the changes that happened to a particular file.\
$ git annotate filename
