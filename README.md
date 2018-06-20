# Trading engine development repository

The bcx repository contains the master as well as development branches of the
Axlantic trading engine project. Each collaborator has writing and reading
permissions to their development branch while only the Axlantic account,
,administered by Håkan Holmberg, has reading and writing permissions to the
master branch.

## Git / Github instructions for bcx repository

These instruction will let you:

1 - Make your first commit to your development branch


## Install trading engine dependencies

The trading engine project is based upon

In order to make a first commmit you need to do the following

### Accept the invitation from Axlantic with your collaborator account.

You should receive an invitation to collaborate from The Axlantic account
that you need to accept. Upon acceptin the invitaion you will gain access to you
development branch of the bcx repository. 
 
# Prerequisities

The trading engine platform should be developed within a virtual environment, in
order to keep track of dependencies. In order to setup a virtual environment you
need the python package virtualenv which can be installed by the following
terminal command:

'''sudo pip3 install virtualenv''' 

You also need git. On ubuntu (linux), git can be installed by issuing the following command in the terminal.

'''sudo apt-get install git''' 

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
