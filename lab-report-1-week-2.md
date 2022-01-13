# Remote Access

This webpage will teach you how to undergo the Remote Access process for CSE15L!

## 1. Installing VScode
The first step is installing VScode onto your device. This is because we will be using the terminal in VScode to execute our commands. If you do not have VScode downloaded on your device yet, you should follow the instructions on the [Visual Studio website](https://code.visualstudio.com/). When VScode is opened it should look like this: 
![VScode image](VScode.png)

Now VScode has been successfully installed! 

## 2. Remotely Connecting
To remotely connect to the server needed for this class, you must first find out your account name for this class at [this link](https://sdacs.ucsd.edu/~icc/index.php). When you find your account, you must change the password to access it. After changing the password, you can finally connect to the server. 

To connect you must open the terminal at VScode by clicking the New Terminal option in the Terminal menu. Then you must type this command: 

```
ssh <your account>@ieng6.ucsd.edu
```
An example would be: 

```
ssh cs15lwi22ake@ieng6.ucsd.edu
```
You would then be prompted for your password, then logged in. If this is your first time logging in, you would need to grant access by entering "y". 

When logging in the terminal should look like this: 

![Terminal1](terminal1.png)
![Terminal2](terminal2.png)

Now you have successfully remotely connected. 

## 3. Trying some commands 

Since we have successfully remotely connected, we can now try to execute some commands! 

* To see a list of your directory contents, try: 
```
ls
```
![ls](ls.png)

There are commands that can be added to the end of other commands to make it more specific. For example: 
```
ls -a
```
Where it lists out all the files. 
![lsa](lsa.png)
```
ls - lat
```
Where it lists out all the files as long as the time stamps and orders it based by the time created. 
![lslat](lslat.png)

* To make a new directory, try: 
```
mkdir <folder name>
```
![mkdir](mkdir.png)
* To change directory, try:
```
cd <directory>
```
![cdtest](cdtest.png)
To return back to the home directory do:
```
cd
```
![cd](cd.png)
* To delete a directory, try: 
```
rm -r <directory>
```
![rm](rm.png)
