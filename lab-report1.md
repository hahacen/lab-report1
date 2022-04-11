**1. Installing the VScode**
- first go to this [Website](https://code.visualstudio.com/)
- follow the instructions and download the right version of VScode in your computer
- ![VScode1](https://github.com/hahacen/lab-report1/blob/main/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202022-04-10%2017.33.30.png)


**2. Remotely Connecting**
if you are in MAC:
- open the VScode and open the terminal
- then type in "$ ssh cs15lsp22zz@ieng6.ucsd.edu", replacing zz with your specifc account
- if it is your first time of connection, the following message is likely to pop up:

 **The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
 RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.  
 Are you sure you want to continue connecting (yes/no/[fingerprint])?**

- then you type "yes" and press enter, then give your password
- the following is likely to be your whole input and output
- ![connect](https://github.com/hahacen/lab-report1/blob/main/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202022-04-10%2017.45.30.png)


**3. Trying Some Commands**
- now you can try some Commands 
- here are some commands that you can try 

- cd ~
- cd
- ls -lat
- ls -a
- cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/

note: if you want to exit, you can 
- Ctrl-D
- Run the command exit


4. Moving Files with scp
- you can first creat a file using the following code
  _class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}_

- then save this file and input the following as command
- scp _WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/_


5. Setting an SSH Key



6. Optimizing Remote Running
