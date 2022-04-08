# Lab Report 1

## Installing VS Code
* open this [link](https://code.visualstudio.com/) and hit download!
* follow any on screen setup instructions

![Image](Screen%20Shot%202022-04-01%20at%208.13.38%20AM.png)

---

## Remotely Connecting
* find your account name [here](https://sdacs.ucsd.edu/~icc/index.php)
* open terminal and run 
```
ssh cs15lsp22zz@ieng6.ucsd.edu
``` 
where `zz` is replaced the letters specific to your username

* type `yes` to any messages and enter password when prompted

![Image](Screen%20Shot%202022-04-01%20at%209.13.16%20AM.png)

---

## Trying Some Commands
* `pwd` prints working directory
* `ls` lists the files in the current directory
  * `ls -a` shows hidden files
* `cd` changes directory
*  `mkdir` makes a new directory

![Image](Screen%20Shot%202022-04-08%20at%209.32.02%20AM.png)

---

## Moving Files with `scp`
* in the terminal, navigate to the directory where the file is located
* run the command  
```
scp fileName.java cs15lsp22zz@ieng6.ucsd.edu:~/
``` 
with your username to move the file to the remote computer

![Image](Screen%20Shot%202022-04-08%20at%2010.23.15%20AM.png)

---

## Setting an SSH Key
* in the client terminal, run the command `ssh-keygen`
* save the key in 
```
/Users/<user-name>/.ssh/id_rsa
```
* when prompted for a password, type nothing an press enter
* in the server, run `mkdir .ssh` to make a directory to copy the key to
*  back in the client, run 
```
scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys
``` 
to finish setting up the key

![Image](Screen%20Shot%202022-04-08%20at%2011.49.30%20AM.png)

---

## Optimizing Remote Running
* after an `ssh` command, you can use quotes to directly run it
```
ssh cs15lsp22abv@ieng6.ucsd.edu "ls"
```
![Image](Screen%20Shot%202022-04-08%20at%2012.17.36%20PM.png)
* use semicolons to run multiple commands on the same line
```
javac WhereAmI.java; java WhereAmI
```

![Image](Screen%20Shot%202022-04-08%20at%2012.16.36%20PM.png)

* use the up arrow to recall previous commands

---

(all instructions above are for mac users; windows instructions may differ)

![Image](https://media.discordapp.net/attachments/561057869051723821/962058262692372510/unknown.png)