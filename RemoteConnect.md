
# Connecting Remotely

In this class you will need to connect to a remote computer on campus. Here is where I will show you how to do this.

First you will need to install OpenSSH, which a good tutorial can be found [here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse).

After this, you will need to get your specific CSE15L remote account from this site [here](https://sdacs.ucsd.edu/~icc/index.php).
It will look something like this: 

cs15lwi22zz@ieng6.ucsd.edu

The first 5 characters will be the same as the example above, along with everything including and after the @. Before you do anything, you'll have to change your password for that remote account. Do so, then wait approximately 15 minutes for the change to go through. After, copy the address, as it will be important for logging in remotely.

Now that that's done, open up a terminal in Visual Studio, then type the command:

*ssh (your remote account from above)*

When doing this for the first time, a message will pop up asking you if you are sure you wish to connect. Type yes and hit enter. You'll immediately be prompted to enter your password. Do so, but know that it will not show you inputting your password, so you'll have to enter it blindly for the purposes of security.

Once that's all done, you should get a message that you've connected and you are done with this step! From here you can input ctrl + D or enter quit to quit from the remote host. [Next, it's time to learn some commands!](Commands.md)