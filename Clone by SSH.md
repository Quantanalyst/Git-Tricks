# How to avoid entering username and password after every push?

A common mistake is cloning using the default (HTTPS) instead of SSH. You can correct this by going to your repository, clicking "Clone or download", then clicking the "Use SSH" button above the URL field and updating the URL of your origin remote like this:

git remote set-url origin git@github.com:username/repo.git


Another trick to avoid entering username/password is setting up a credential cacher: https://help.github.com/articles/caching-your-github-password-in-git/. This way you can skip entering your username-password for the time period you are working with your LFS-tracked files. 
