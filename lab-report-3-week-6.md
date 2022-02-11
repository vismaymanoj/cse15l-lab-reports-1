# Lab Report 3 - Streamline ```ssh``` Configuration
## 1. Edit your config file

I edited my config file in VSCode. I simply located my .ssh folder and opened the text file: config. This is the original contents:

![image](https://myang25.github.io/cse15l-lab-reports/lab3-pictures/lab3-img1.png)

To log-in with an alias, we enter the text:

```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lwi22zzz (use your username)
    IdentityFile ~\.ssh\id_rsa (I am a Windows user)
```

![image](https://myang25.github.io/cse15l-lab-reports/lab3-pictures/lab3-img2.png)

Save the file, and now if you open a new terminal, you should be able to sign into your ieng6 account with only the following command:

```
> ssh ieng6
```

## 2. Logging in with an alias

This is an example of a sucessful login using the alias.

![image](https://myang25.github.io/cse15l-lab-reports/lab3-pictures/lab3-img3.png)

Keep in mind that the alias can be anything you want it to be. Just change the ```ieng6``` after ```Host``` to whatever you want the alias to be.

## 3. Running the scp command with an alias

You can also copy files onto the server with an alias. Here, I have created a TestFile.java. Without signing in, I can run ```scp <FileName.type> alias``` to copy the file. 

Here is the file being copied:

![image](https://myang25.github.io/cse15l-lab-reports/lab3-pictures/lab3-img4.png)

(I moved the file to the wrong file directory the first time; thats why it failed)