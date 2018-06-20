# Trading engine development repository

The bcx repository contains the master as well as development branches of the
Axlantic trading engine project. Each collaborator has writing and reading
permissions to their development branch while only the Axlantic account, administered by Håkan Holmberg, has reading and writing permissions to the
master branch.

## Git / Github instructions to the bcx repository

These instruction will let you commit to your development branch of the bcx repository.

### Accept the invitation from Axlantic with your collaborator account.

You should receive an invitation to collaborate from the Axlantic account
that you need to accept. Upon accepting the invitation you will gain access to you
development branch of the bcx repository. 
 
### Prerequisites

The trading engine platform should be developed within a virtual environment in
order to keep track of dependencies. In order to setup a virtual environment you
need the python package virtualenv which can be installed by the following
terminal command.

```
sudo pip3 install virtualenv
```

You also need git. On ubuntu (linux), git can be installed by issuing the following command in a terminal.

```
sudo apt-get install git
``` 

### Clone the bcx master branch

After installing git you will be able to clone the master branch of the bcx repository from the
Axlantic account. It is important that you are positioned in the folder where you want to
store the project i.e., if you want to store the bcx repository in ~/dev you
should be postioned at ~/dev. To clone the master branch, issue the following
command in a terminal.

```
git clone https://github.com/Axlantic/bcx.git
```

This will create a local copy of all branches of the bcx repository, including yours, on your computer.

### Activate the virtual environment 

The bcx repository already includes a virtual environment so the only thing you
need to do is to activate it. In a terminal, position yourself in your local copy of the bcx repository (for
example ~/dev/bcx) and issue the following command.

```
source env/bin/activate
```

You will now see (env) before your username in the terminal window. From now on,
we will continue to work in the virtual environment which means that all commands
will be issued in the terminal that is connected to the virtual environment.

### Configure the git repository
Your local branch includes a git repository that needs to be configured. We need
to tell the Axlantic account which user that is committing to the
bcx repository. This can be done by issuing the following commands in the
designated terminal

```
git config --global user.name "yourusername"
git config --global user.email "youremail"
```

### Create your first test commit to your branch of the bcx project

Create a text file "misc.txt" in your local copy and add the line "My first commit" (and save it). After creating the text file, issue the following commands in a terminal.

```
git fetch --all
git branch
```

Now you should see the master branch and it should be the active branch (have a * next to it). You need to switch to your branch which is done by issuing the folloing command

```
git checkout <yourbranch> 
```

Now you are ready to commit misc.txt to your branch by issuing the following commands

```
git add . 
git commit -m "my first commit"
git push bcx <yourbranch>
```

Finally, go to the Axlantic account on Github where you should be able to see
your commit in the bcx repository.

The ` git add .` command adds all files in the repository for staging (a file
needs to be staged before it can be pushed). This is in general not a good practice
since it will always push every package that is installed in the virtual
environment. Instead, you should only stage the files that needs to be pushed and
include a requirements.txt file that contains all dependencies. The
requirements.txt file should be located in the root directory (bcx in this case). To print a
requirements.txt file you need to install the freeze package and execute the command

```
pip freeze > requirements.txt
```

# Useful git commands

You can save your login information issuing the following commands.

```
git config --global credential.helper "cache --timeout=3600"

```

This will make git store your password in cache for the number of seconds
specified by the timeout option.


# Starting the django development server and inspecting the trading engine GUI

In order to start the django development server you need to position yourself in
bcx/django-gentelella/gentelella and execute the following terminal command.

```
python manage.py runserver

```

This will start the development server and you will be given an output such as


```
System check identified no issues (0 silenced).
June 20, 2018 - 12:53:59
Django version 1.10, using settings 'gentelella.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.

```
In order to see the tradding engine GUI you simply copy the url (in this case
http://127.0.0.1:8000/) and paste it in you web browser.



