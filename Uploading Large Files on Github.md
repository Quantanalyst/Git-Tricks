# Uploading Large Files to Github

GitHub has a strict file limit of _100MB_. If you are just uploading lines of codes, this is not something that you need to worry about. However, if you want to upload a bit of data, or something in binary, this is a limit that you might want to cross. Here are three different ways to overcome the 100MB limit.

1. **.gitignore**
Create a file .gitignore in the parent directory of the repository, and store all the file directories that you want Git to ignore. Use * for wildcard so that you do not need to add file directories manually each time you create a new large file. Here is an example:\
*.nc\
*.DS_store\
These ignored files will be automatically ignored by Git and will not be uploaded to GitHub. No more error messages.

2. **Repository Cleaner**
If you have accidentally committed files locally that exceeds 100MB, you would have a hard time trying to push it to GitHub. It cannot be solved by removing the large files and committing again. This is because GitHub keeps track of every commit, not just the latest one. You are technically pushing files in your entire commit record.\
While you could technically resolve it by branching, it is by no means straightforward. Fortunately, you can run a repository cleaner and it automatically cleans all the large file commits.\
Download BFG Repo-Cleaner bfg.jar and run the following command:\
**$** java -jar bfg.jar --strip-blobs-bigger-than 100M <your_repo>\
It automatically cleans your commits and produces a new commit with the comment ‘remove large files’. Push it and you are good to go.

3. **Git LFS**
You might have noticed that the abovementioned methods both avoid uploading the large files. What if you really want to upload them so that you could gain access to them on another device?
Git Large File Storage lets you store them on a remote server such as GitHub. Download and install git-lfs by placing it into your $PATH. You will then need to run the following command once per local repository:
**$** git lfs install\
Large files are selected by:\
**$** git lfs track '*.nc'\
**$** git lfs track '*.csv'\
This will create a file named .gitattributes, and voilà! You can perform add and commit operations as normal. Then, you will first need to a) push the files to the LFS, then b) push the pointers to GitHub. Here are the commands:\
**$** git lfs push --all origin master\
**$** git push -u origin master
