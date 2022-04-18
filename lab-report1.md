**1. Installing the VScode**
- first go to this [Website](https://code.visualstudio.com/)
- follow the instructions and download the right version of VScode in your computer
![VScode1](https://github.com/hahacen/lab-report1/blob/main/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202022-04-10%2017.33.30.png)

- and you will see the following page of VScode

![VScode2](https://github.com/hahacen/lab-report1/blob/main/481649652336_.pic.jpg)

**2. Remotely Connecting**

if you are in MAC:
- open the VScode and open the terminal
- then type in ```$ ssh cs15lsp22zz@ieng6.ucsd.edu"```, replacing zz with your specifc account
- if it is your first time of connection, the following message is likely to pop up:

 ```The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.```
 
 ```RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.```
 
 ```Are you sure you want to continue connecting (yes/no/[fingerprint])?```

- then you type ```yes``` and press enter, then give your password
- the following is likely to be your whole input and output
- ![connect](https://github.com/hahacen/lab-report1/blob/main/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202022-04-10%2017.45.30.png)


**3. Trying Some Commands**
- now you can try some Commands 
- here are some commands that you can try 

- ```cd ~```
- ```cd```
- ```ls -lat```
- ```ls -a```
- ```cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/```

note: if you want to exit, you can 
- ```Ctrl-D```
- ```Run the command exit```

for example, if you try some, you may see the following in the terminal
![pic](https://github.com/hahacen/lab-report1/blob/main/471649652063_.pic.jpg)

**4. Moving Files with scp**
- you can first creat a file using the following code
  
  ```class WhereAmI {
  
  _public static void main(String[] args) {_
  
    _System.out.println(System.getProperty("os.name"));_
    
    _System.out.println(System.getProperty("user.name"));_
    
    _System.out.println(System.getProperty("user.home"));_
    
    _System.out.println(System.getProperty("user.dir"));_
    
  _}```
  
_}_

- then save this file and input the following as command in the terminal of the directory that you created and saved the file
- scp _WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/_
- then this file will be moved to the remote server
- you may see the following output in the terminal of the directory that you created and saved the file
- ![output](https://github.com/hahacen/cse15l-lab-reports/blob/main/451649647571_.pic.jpg)

cs15lsp22amu@ieng6.ucsd.edu


**5. Setting an SSH Key**
- open the terminal in VScode and you can input the following commands


on client (your computer)
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
Enter passphrase (empty for no passphrase): 
Note: Make sure that you do not add a passphrase for this step.
Enter same passphrase again: 
Your identification has been saved in /Users/<user-name>/.ssh/id_rsa.
Your public key has been saved in /Users/<user-name>/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:jZaZH6fI8E2I1D35hnvGeBePQ4ELOf2Ge+G0XknoXp0 <user-name>@<system>.local
The key's randomart image is:
+---[RSA 3072]----+
|                 |
|       . . + .   |
|      . . B o .  |
|     . . B * +.. |
|      o S = *.B. |
|       = = O.*.*+|
|        + * *.BE+|
|           +.+.o |
|             ..  |
+----[SHA256]-----+


- it should look like![terminal1](https://github.com/hahacen/cse15l-lab-reports/blob/main/461649651061_.pic.jpg)

- then you copy the key from the public server to your .ssh your account server
 
$ ssh cs15lsp22zz@ieng6.ucsd.edu
 
<Enter Password>
 
 
$ mkdir .ssh
 
$ <logout>
 

$ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys
 
You use your username and the path you saw in the command above

 
 
**6. Optimizing Remote Running**
 
- using the following code is the fastest way to make a local edit, then copy it to the remote server and then run it.
 
 scp WhereAmI.java cs15lsp22amu@ieng6.ucsd.edu:～/
 
 ssh cs15lsp22amu@ieng6.ucsd.edu "javac WhereAmI.java;java WhereAmI"

 
 
 
