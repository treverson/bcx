# bcx
Trading engine development repository
# Git / Github instruction s for bcx repository

# First commit of repository

1 - Create a github repository
2 - Invite collaborator accounts to the project using the main account (the account that owns the repository). You should include your personal user account as one of the collaborator accounts
3 - Accept the invitation with your collaborator account.
4 - Push the first commit of your local repository to the main account repository
5 - Create one development branch for each collaborator
 

# Prerequisities

1 - Invitation from Axlantic to your github account
2 - Confirmation from you with respect to the invitation
3 - The python package virtualenv. On linux, you can install the package using the following command in the terminal.

sudo pip3 install virtualenv 

4 - You need git. On ubuntu (linux), git can be installed by issuing the following command in the terminal.

sudo apt-get install git 

# Push a first test commit to your branch of the bcx repository.

1 - Clone the bcx master branch from the Axlantic account by issuing the following command in terminal (the command should be issued in the folder where you want to store the project i.e., if you want to store the bcx repository in ~/dev you should be postioned at ~/dev).

git clone https://github.com/Axlantic/bcx.git

This will create a local copy of all branches of the bcx repository on your computer.

2 - Activate the virtual environment by issuing the following command (you need to be positioned in you local copy the bcx repository i.e., ~/dev/bcx).

source env/bin/activate

3 - Configure the git repository, that was included in your local copy of the bcx repository, by issuing the following command in terminal

git config --global user.name "yourusername"

git config --global user.email "youremail"

This tells the Axlantic account which user that is trying to commit to the different branches of the bcx repository.
  
4 - Create your first test commit to your branch of the bcx project by creating a text file "misc.txt" in your local copy and add the line "My first commit" (and save it). After creating the text file issue the following commands in a terminal.

git fetch --all
git branch

Now you should see the master branch and it should be the active branch (first line to printed).

5 - You need to switch to your branch which is done by issuing the folloing command

git checkout <yourbranch> 

6 - Now you  are ready to commit misc.txt to your branch by issuing the following commands

git add . 
git commit -m "my first commit"
git push bcx <yourbranch>

7. You should now be able to see your commit in the bcx repository in the Axlantic account.
