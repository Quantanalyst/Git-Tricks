# How to create a public SSH key for your computer

In order to avoid entering your username and password each time you push your updates to your github, you need to give your public SSH key to your Github account to autenticate your computer. However, first you need to generate one for your computer. 

In order to provide a public key, each user in your system must generate one if they don’t already have one. First, you should check to make sure you don’t already have a key. By default, a user’s SSH keys are stored in that user’s ~/.ssh directory. You can easily check to see if you have a key already by going to that directory and listing the contents:\
**$** cd ~/.ssh\
**$** ls\
_authorized_keys2  id_dsa       known_hosts
config            id_dsa.pub_\

You’re looking for a pair of files named something like id_dsa or id_rsa and a matching file with a .pub extension. The .pub file is your public key, and the other file is the corresponding private key. If you don’t have these files (or you don’t even have a .ssh directory), you can create them by running a program called **ssh-keygen**, which is provided with the SSH package on Linux/macOS systems and comes with Git for Windows:

**$** ssh-keygen -o\
Generating public/private rsa key pair.\
Enter file in which to save the key (/home/saeed/.ssh/id_rsa):\ 
Enter passphrase (empty for no passphrase):\
Enter same passphrase again:\
Your identification has been saved in /home/saeed/.ssh/id_rsa.\
Your public key has been saved in /home/saeed/.ssh/id_rsa.pub.\
The key fingerprint is:\
SHA256:Z7I8VGTJcwsmQ+dKipu2BWAEDTcz/U4LNquGwVZVfN8 saeed@saeed-ThinkPad-X1-Carbon\

First it confirms where you want to save the key (.ssh/id_rsa), and then it asks twice for a passphrase, which you can leave empty if you don’t want to type a password when you use the key. However, if you do use a password, make sure to add the -o option; it saves the private key in a format that is more resistant to brute-force password cracking than is the default format. You can also use the ssh-agent tool to prevent having to enter the password each time.

Now, each user that does this has to send their public key to you or whoever is administrating the Git server (assuming you’re using an SSH server setup that requires public keys). All they have to do is copy the contents of the .pub file and email it. The public keys look something like this:

**$** cat ~/.ssh/id_rsa.pub\
ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAklOUpkDHrfHY17SbrmTIpNLTGK9Tjom/BWDSU
GPl+nafzlHDTYW7hdI4yZ5ew18JH4JW9jbhUFrviQzM7xlELEVf4h9lFX5QVkbPppSwg0cda3
Pbv7kOdJ/MTyBlWXFCR+HAo3FXRitBqxiX1nKhXpHAZsMciLq8V6RjsNAQwdsdMFvSlVK/7XA
t3FaoJoAsncM1Q9x5+3V0Ww68/eIFmb1zuUFljQJKprrX88XypNDvjYNby6vw/Pb0rwert/En
mZ+AW4OZPnTPI89ZPmVMLuayrD2cE86Z/il8b+gw3r3+1nKatmIkjn2so1d01QraTlMqVSsbx
NrRFi9wrf+M7Q== schacon@mylaptop.local








