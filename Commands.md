
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

[Return to the Table Of Contents](index.md)
