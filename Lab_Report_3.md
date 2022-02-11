# Copy Whole Directories with scp -r

As stated in the title, you can use scp -r to recursively copy all files and directories of a certain directory. This is best done by doing something akin to

![scp -r](https://i.ibb.co/zJ1T4cg/Screenshot-2022-02-10-164013-PNG.jpg)

First it will ask for the password, and after that password is input correctly, tt will display the files it attempts to copy over (Which within this example is a lot) and copy them over. Once that is done, you can change directory into the new directory and run commands as you see fit, like such:

![javacJava](https://i.ibb.co/JpQNX7S/Screenshot-2022-02-10-164030.jpg)

But, this is a LOT of work, but as we learned earlier in lab 1, we can easily optimize this process all into one line. Which will end up looking like this!

![AllInOne](https://i.ibb.co/2dQvqrC/all-in-one-line.png)

[Back to the Table of Contents!](index.md)