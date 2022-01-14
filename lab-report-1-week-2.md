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

Next, open up a new file by clicking "New File". Then, navigate to the top toolbar and select "Terminal" and "New Terminal". This should open a terminal input at the bottom where you can issue the command:

$ ssh cs15lwi22xxx@ieng6.ucsd.edu
<br/>

If this is your first time connecting to the server, you will get a message confirming if you are sure you would like to connect onto this server. Just put "yes" and don't ask questions.
<br/>

Then the terminal will ask for your password, which is your school account password that you just reset. Keep in mind that the password will be invisible, which trips me up every time. If your password is correct, you should see something along the lines of:
<br/>

![image](https://myang25.github.io/cse15l-lab-reports/Login%20ieng6.png)
<br/>

## 3. Trying Some Commands
<br/>

Now that you are logged in and connected to the server, you can try out some commands! You can try some of these commands on both the cleint (your own computer) and the server (the ssh remote computer).

* ls
* cd
* ls ~a
* cd <A directory>
<br/>

This is an example of what some commands may return:
<br/>

![image](https://myang25.github.io/cse15l-lab-reports/Trial-Commands.png)
<br/><br/>

## 4. Moving Files with SCP
<br/>


