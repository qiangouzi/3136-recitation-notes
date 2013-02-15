# Recitation 4 #

## 'Git' er Done ##

### What's git? ###

Git is a distributed revision control and source code management system with an emphasis on speed.
    
### Make a Data Structures Directory ###

If you haven't already, please make a 3136 directory on your clic account with the following command in your home directory:

    mkdir 3136
    
Change into the directory with the command:

    cd 3136

### Configuring git ###

So in order to use git, you must first let it know who you are.  Do this by telling git your name and email:

    git config --global user.name "Jae Woo Lee" 
    git config --global user.email jae@cs.columbia.edu

Now, put the directory under git revision control with the command:

    git init

### Repositories and Retrieving Assignments ###

A git repository is a place to store fun stuff like code, projects, and in our case recitation notes, homework skeleton code, or homework solutions for you!  Github.com is a website where users make repositories to share and update code with one another.

Once Jae has added the skeleton code for your assignment, you will be able to clone his skeleton code from his repository with the command:

    git clone /home/jae/cs3157-pub/lab1 lab1
    
Once the labs have all been submitted, Jae will post the solutions to his repository.  You can retrieve them with the command:

    git pull
    
from with in the lab1 subdirectory.

### The 4 levels of Commitment ###

A file in a directory under git revision control is part of one of four "levels of commitment".  They are:

    untracked
    tracked and unmodified
    tracked, modified, and unstaged
    tracked, modified, and staged

You can check the level of commitment of the files in a directory under git revision control with the command:

    git status

An untracked file is a file that is not being watched for modifications by git revision control.
To track a file, enter the following command:

    git add filname

Keep in mind that you only want to be tracking files that you will be editing again or submitting.  For most programming labs in this course, it will include the .h, .c, Makefile and README.txt files in the directory.  The executable and .o files need not be tracked.

A tracked and unmodified is a file that has been tracked and not modified since its inception or since the last commit.

A tracked, modified, and unstaged file is a file that had been tracked, edited since the last commit, but not staged for commit since the last commit.
To stage the file for commit, again enter the command:

    git add filename

A tracked, modified, and staged file is a file that has been tracked, edited since the last commit, and stage for commit.

### Committing Changes ###

To commit changes to your files that are tracked, modified, and staged, enter the command:

    git commit -m "a message with notes about the commit"
    
from your lab1 directory.
To see your detailed commit history, enter the command:

    git log -p --color

### Submitting labs ###

You can submit a lab with the submit-lab script:

    /home/w3157/submit/submit-lab  lab1

from the lab1 directory.