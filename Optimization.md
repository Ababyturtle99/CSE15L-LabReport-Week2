
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

*cp program.java; javac program.java; java program*

Finally, there's one last time saving tip. When in the terminal, you can press the up and down arrows to move between any of the commands that you have previously entered. This can allow you to re run commands after any changes to the code, or not have to retype a full command to change one part of it.

[Return to the Table Of Contents](index.md)
