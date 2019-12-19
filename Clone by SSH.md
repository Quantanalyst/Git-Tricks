# How to avoid entering username and password after every push?

A common mistake is cloning using the default (HTTPS) instead of SSH. You can correct this by going to your repository, clicking "Clone or download", then clicking the "Use SSH" button above the URL field and updating the URL of your origin remote like this:

git remote set-url origin git@github.com:username/repo.git



