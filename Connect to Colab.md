# Connecting your private Git repo to your Colab account

1. **Using Google Drive:**\
When you are using Colab for running your Deep Learning models the most obvious way to access the large datasets is by storing them on Google Drive and then mounting Drive onto the Colab environment.

2. **Using a Public Git repository (without SSH):**\
The integration is just a couple of lines — when the git repository you want to clone is a public one.\
  * Mount Google Drive on to your Colab environment.
    * from google.colab import drive
    * drive.mount('/content/drive')

On executing the above 2 lines, you will be prompted to go to the Google Accounts URL as shown, for authenticating. Click on the URL displayed in the Output section of the notebook cell. This takes you to a page that asks your permission. After granting permission, you will receive a code that you must enter into the authorization code section on your colab notebook and click ENTER. Google Drive is now mounted and you get the message confirming that.\
You can then set any of your Drive folders as your working directory. Then clone the public git repo in to your working directory. These two steps are implemented as below:\
  import os
  os.chdir('/content/drive/My Drive/Deep Learning Projects')
  !git clone https://github.com/Quantanalyst/Kaggle-Competitions

3. **Clone a Private Git Repo (using SSH):**\
Unfortunately, you cannot clone your private repositories as easily. As a matter of fact, you can pull off a one-liner in that case as well as shown below:\
!git clone https://username:password@github.com/username/repository.git\

That is, provide your username:password along with the repository link to clone a private repository. This works, but the catch is that the password gets stored in git/config and in your bash history logs. Therefore it is not advisable to clone your private repos in the above manner. Instead we will be using the SSH protocol to connect your private github/gitlab repo to colab.



