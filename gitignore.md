# .gitignore tricks

Q: why .gitignore ignore my files?

Answer: **.gitignore** only ignores files that are not part of the repository yet. If you already git added some files, their changes will still be tracked. To remove those files from your repository (but not from your file system) use git rm --cached on them.
