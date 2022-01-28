# Installing Visual Studio Code

First, You'll want to download the installer from [Visual Studio Code's website](https://code.visualstudio.com/download).

Be sure to install the one for your specific operating system!

![VSCWebsite](https://i.ibb.co/Hh0rMfh/VSCImage.png)

After you've done that and the installer is downloaded, run the installer and change the settings to what you wish,
such as install location, and have it launch when it finishes.

You'll want to go to the 5th tab down on the left side to install add ons to work with the programming languages you choose.

![VSCAddons](https://i.ibb.co/414Cx2r/VSCaddons.png)

Use the searchbar to search for add ons that you prefer. Whether it's Java, C#, or javascript, install the add ons and you'll be good to start working in Visual Studio Code! To learn about remote connecting, you can continue to [here](RemoteConnect.md).


# Connecting Remotely

In this class you will need to connect to a remote computer on campus. Here is where I will show you how to do this.

First you will need to install OpenSSH, which a good tutorial can be found [here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse).

After this, you will need to get your specific CSE15L remote account from this site [here](https://sdacs.ucsd.edu/~icc/index.php).
It will look something like this: 

cs15lwi22zz@ieng6.ucsd.edu

The first 5 characters will be the same as the example above, along with everything including and after the @. Before you do anything, you'll have to change your password for that remote account. Do so, then wait approximately 15 minutes for the change to go through. After, copy the address, as it will be important for logging in remotely.

Now that that's done, open up a terminal in Visual Studio, then type the command:

```*ssh (your remote account from above)*

When doing this for the first time, a message will pop up asking you if you are sure you wish to connect. Type yes and hit enter. You'll immediately be prompted to enter your password. Do so, but know that it will not show you inputting your password, so you'll have to enter it blindly for the purposes of security.

Once that's all done, you should get a message that you've connected and you are done with this step! It should look something like this:

![RemoteConnection](https://i.ibb.co/9NkGRbg/Remote-Connect.png)

From here you can input ctrl + D or enter quit to quit from the remote host. [Next, it's time to learn some commands!](Commands.md).


# Commands and More

This section will cover 2 things, trying new commands, and copying files over.

# A Few Basic Commands

Feel free to mess around and use these commands yourself to try to get familiar with them! Notice how they will show different outputs based on whether you are on the remote connection or not.

```ls = lists files

```pwd = shows the directory of the current file

```mkdir (folder name) = make a new folder in that directory

```cp (File) = copy a file over

```cd (directory) = change directory to the directory provided in the argument
```cd ~ = ~ is short for home in this case, and will take you to the home folder

```dir = shows the available directories

![dirCommand](https://i.ibb.co/kxCB9qh/Commands.png)

It's possible to also run commands while connected to the server, although the files must be on the remote server.
You can do this how you would normally do so, such as running javac file.java then java file

# Copying Files Over

When connected to the remote server, you may copy files over onto it by using the scp command above. Doing so will allow you to run these commands on the remote server. Doing so is as simple as this command.

```*scp (file)*

![CopyFiles](https://i.ibb.co/7b9mgsz/Copying-files.png)

Now your file is on the remote host! From here, you can put whatever files you want, run them, or you can [Learn about how to optimize your commands](Optimization.md).


# Optimization

Here I will show some ways to help optimize running commands, including setting an SSH key, and optimizing how you can run commands.

# SSH Keys

Creating and using an SSH key properly can help you run commands faster by not requiring you to put in your password every time you wish to log in on the computer which you created the key on. To start, you'll want to enter *ssh-keygen*

What this does is create a pair of keys, a public and a private. It will ask you where you would like to save the key. Enter in the directory where you wish to save it. You will be prompted to enter your password, and doing so will bring up a result simiilar to this:

![SSHkeygen](https://i.ibb.co/6JW7wgv/SSH-Keygen.png)

For Windows users, there will be a bit more you have to do, as well detailed [here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation). Once you're past this, you'll want to use the scp command to copy the public key over onto the remote host. Doing this will then allow you to log in on that computer without needing to log in every time.

# Optimize Running Commands

Now that you can connect to the remote host faster, let's optimize our commands just a little bit. First you can connect to the remote host, run any command from there, and them immediately exit it by inputting a command as such: 

![commandsremote](https://i.ibb.co/86CDrwf/Optimize.png)

Make sure to put the command you want to run in quotes!

Another way to help optimize running commands is by running multiple commands within the same line, which can be done by separating each command with semicolons. For example, this allows you to use javac and java to compile all files and run it in one line. You can copy over files and run them in one line, just like this! 

```*cp program.java; javac program.java; java program*

![multiple commands](https://i.ibb.co/8Y9FhDf/important-picture-for-lab1.png)

Finally, there's one last time saving tip. When in the terminal, you can press the up and down arrows to move between any of the commands that you have previously entered. This can allow you to re run commands after any changes to the code, or not have to retype a full command to change one part of it.

[Back to the title!](index.md)

