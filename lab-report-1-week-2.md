# How to Log-in to ieng6!

To log in into your course specific account on ieng6 is not that hard! Just follow the simple steps below. Image screenshots provided for visual assistance.
<br/><br/>

## 1. Installing VSCode
---
![Image](https://myang25.github.io/cse15l-lab-reports/Install%20VSCode.png)
<br/>
Go ahead and head to this link to download VSCode for whichever processing system your particular laptop/PC uses:

[Download VSCode](https://code.visualstudio.com/download)

Then simply follow the installer wizard's instructions and your ready for the next step.
<br/><br/>

## 2. Remotely Connecting
[FOR WINDOWS USERS ONLY! - YOU NEED TO DOWNLOAD A PROGRAM CALLED OPENSSH. THE INSTRUCTIONS ARE IN THIS LINK: [Install OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) ]
<br/><br/>

Then, you need to find your course-specific account for the class you are attending that is using ieng6. The 3 letter code is found here: [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php). It may ask you to reset the password to the account in order to verify your identity. After the password is reset, it may take a while for the new password to take effect.
<br/>

Next, navigate to the top toolbar and select "Terminal" and "New Terminal". This should open a terminal input at the bottom where you can issue the command:

**$ ssh cs15lwi22xxx@ieng6.ucsd.edu**
<br/>

If this is your first time connecting to the server, you will get a message confirming if you are sure you would like to connect onto this server. Just put "yes" and don't ask questions.
<br/>

Then the terminal will ask for your password, which is your school account password that you just reset. Keep in mind that the password will be invisible, which trips me up every time. If your password is correct, you should see something along the lines of:
<br/>

![image](https://myang25.github.io/cse15l-lab-reports/Login%20ieng6.png)
<br/><br/>

## 3. Trying Some Commands
<br/>

Now that you are logged in and connected to the server, you can try out some commands! You can try some of these commands on both the cleint (your own computer) and the server (the ssh remote computer).

* ls
* cd
* ls ~a
* cd [directory]
<br/>

This is an example of what some commands may return:
<br/>

![image](https://myang25.github.io/cse15l-lab-reports/Trial-Commands.png)
<br/><br/>

## 4. Moving Files with SCP
<br/>

Next, lets try moving a file from our local computer to the server. Create a file in VSCode and write some code into it. Then, save it. Log out of the server. Use the commmand cd [Directory] to navigate to the folder in which that file is saved. Run the following command:

**$ scp FileName.java cs15lwi22xxx@ieng6.ucsd.edu:~/**

This command copies the file from your computer and places a copy in the server. This command will also prompt your password.

Once you've done that, you can log back in using ssh and run the command **ls**. **ls** lists the current files in selected directory. You should see your new file show up inside. For my example, I used **WhereAmI.java**:

![image](https://myang25.github.io/cse15l-lab-reports/Moved%20File.png)
<br/><br/>

## 5. Setting Up an SSH Key
<br/>

By setting up an SSH Key, we no longer need to type our password whenever we want to login. Run the command:

**$ ssh-keygen**

It will ask for a file to put the password in. The default one is usually fine so just press enter. Then, it will ask you to set up a password for the key. To save time, we leave it blank (just press enter).

[FOR WINDOWS USERS: THERE ARE MORE STEPS FOR YOU HERE: [https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation)]

Next, login into the server. Run the command:

**$ mkdir .ssh**

Logout. Then, on ur client, run:

**$ scp /Users/YourUser/.ssh/id_rsa.pub cs15lwi22xxx@ieng6.ucsd.edu:~/.ssh/authorized_keys**

Now, you should be able to ssh into your account without needing a password.

Finished product should execute something like this:

![Image](https://myang25.github.io/cse15l-lab-reports/SSH%20Key.png)
<br/><br/>

## 6. Optimizing Remote Running
<br/>

To optimize your command efficency, here are some tips and tricks to make your remote operations more enjoyable. 

1. You could put multiple commands into 1 single line of code, seperating each individual command with a semicolon
2. The up arrow is your friend. If you have a command that you used recently and you need it again, just press the up button a few times.
3. Opening 2 terminals sometimes will help organize and see more at once.

For example, the following code is mutiple commands ran from the same line:

![image](https://myang25.github.io/cse15l-lab-reports/Optimization.png)
