## What is 'git' and how to get started?

# What is ```git```?

- ```git``` is a free and open source distributed ```VCS```(version-control-system).
- Today almost all projects whether it is small hobby project or big commercial project, developers use ```git``` for version control.  

#### but wait, what is ```VCS```?  
- [What is VCS?](https://aw-santo.hashnode.dev/what-is-vcs)
do give it a minute...
  
##### so, now we have an idea what is ```VCS```...

### Let's get into ```git```:  

## Installation  
1. For windows
> go to [https://git-scm.com/download/win](https://git-scm.com/download/win) and download the client according to the windows configuration.  
  
2. Fo Linux [Debian]  
```apt-get install git```  
  
3. For macOS  
```brew install git```  
  
  
## Getting started
- Let us have a directory ```git_tuto```, we will play with this directory only.  
to begin with ```git_tuto``` is empty.

![11.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664704934718/Q5OzkeyCj.png align="left")
- Now we have to configure ```git```, set user-name and user-email. This user-email is typically the same as the email linked with [GitHub](https://github.com/) (An internet hosting service for software development and version control using ```git```), but for the sake of this tutorial, we will temporarily set a dummy email.  
  
**go to ```git_tuto``` directory and open terminal or git-bash**  

**setting name as 'san'**  
```git config --global user.name "san"```  

**setting email as 'san@mail.com'**  
```git config --global user.email "san@mail.com"```  

if we do,  
```git config --global --list```  

![12.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664705333678/lJn1Y9-So.png align="left")
  
- Let us start with the command ```git status```. You will be using this command almost at every time, ```git status``` shows the current status of the directory. 
 
```git status```  

![13.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664705365877/ftnDRSmMg.png align="left")

**what happened?**  
We have to first make the current directory a ```git``` maintainable directory.  
We have to initialize the ```git```.  
```git init```  

![14.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664705375471/0UuOmYlKY.png align="left")
 

now if we do:   
```git status```  

![15.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664705385037/SKEGrwg8c.png align="left")


We have initialized ```git``` in ```git_tuto``` directory, now from onwards, we will call this directory a ```repository``` or simply a ```repo``` (a ```git``` initialized directory is typically called ```repository```).The above message tells that there is nothing that has changed, the default branch (a particular stream in a ```repo```) is ```master```, in some cases it may be ```main``` also.

### Let's play  
- let us create two files ```fname.txt``` and ```lname.txt``` in ```git_tuto``` repo.  

```fname.txt``` contains  
> Elon  

```lname.txt``` contains  
> Musk  

- if we do,  
```git status```
![1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664701692871/I1qr7Mia4.png align="left")  
```git``` is telling that both the files ```fname.txt``` and ```lname.txt``` are untracked files, which means ```git``` is not maintaining or counting the changes happening in these files.  
\* All the untracked files will be displayed in 'red' color.  
We have to explicitly tell ```git``` to track these files.  
For that, we have a command ```git add <file-name>```  
\* If we want ```git``` to track all files in the current repo, then we have to do ```git add . ``` , here ' . ' means all files.  

- Let's do ```git add . ```  
**now ```git``` is tracking changes in these files**  

- ```git status```  

![2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664702257209/idX9DnB9f.png align="left")

After doing ```git add . ```, all the files will come into the staging area (which means we have accepted the changes, now we just have to commit (finalize) them.  
\* All the files which are in the staging area will be displayed in 'green' color.  

- To commit or finalize the changes we just have to enter  
```git commit -m "<commit-message>"```  
'-m' flag signifies 'commit-message'.  
**an empty 'commit-message' will abort this operation.**  
```git commit -m "Initial commit"```  

![3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664703018946/QbAipX55p.png align="left")

- ```git status```

![4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664703106165/DV37kAM7x.png align="left")

#### Up to this point, we are tracking two files, and committed the changes in them, means there is nothing to be worried about. Everything is maintained.  
  
#### To see the commit history, we have a command ```git log```  
- ```git log```  
This will list down all the commits we have made in the repo, for our case, it will show
![5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664703408851/Tt7jzeBBH.png align="left")
We can see the 'commit-message' which we have provided as "Initial commit".  
**The long string after 'commit' is called 'commit hash', it is uniquely generated by ```git``` for every commit we make.**

### Now, let's change ```fname.txt``` and recur the above process.  
```fname.txt``` will now contain  
> Jeff  

- ```git status```  

![7.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664704046224/_DZl_QIt2.png align="left")

Now observe, ```git``` is telling that ```fname.txt``` is modified.  
Let add it to the staging area and commit.  
- ```git add fname.txt```
- ```git status```

![8.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664704195842/HQGUE2aHo.png align="left")
- ```git commit -m "fname.txt changed to Jeff"```

![9.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664704296682/fRi--cFxX.png align="left")

- ```git log```

![10.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664704349118/ODRjyTQLD.png align="left")

We have both our commits along with their commit-hashes and other info.  

### Similarly we can change, add,  commit with no limits.

#### These are the basic commands to start with ```git```, it has a lot of other functioning and capabilities too, we will see them eventually.

**Stay tuned!**


> Hope you liked it...

