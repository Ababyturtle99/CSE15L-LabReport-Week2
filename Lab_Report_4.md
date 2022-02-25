# Lab Report 4

For our expected, according to the previews, these are the only links that should be grabbed from the markdown files.

Test 1:

`google.com

google.com

ucsd.edu

Test 2:

a.com(())

example.com

Test 3:

https://ucsd-cse15l-w22.github.io/

And here are the failed tests for [my repository](https://github.com/Ababyturtle99/markdown-parse):

![myRepoFaile](https://i.ibb.co/fD36btq/failed-my-tests.png)

and the failed tests for this [repository](https://github.com/ucsd-cse15l-w22/markdown-parse)

![notMyRepoFail](https://i.ibb.co/tcwdht9/Failed-Copied-tests.png)

In order to solve problems with tick marks, I believe a small code change is possible, where you look for outside the bracket before to see if there is a tick mark and follow up to see if there's another in the same line, causing the format change. If both ende up inside brackets, then it may be ignored, as the program only grabs the links that work within the end result of the md file. However, for the final example in that snippet, "[`code]`](ucsd.edu)" It will be very difficult to find a way to get this link to work without facing other problems, which I will refer to later.

Nested brackets and links are very difficult to deal with, at least without causing other problems. You would need a program that would count and try to even out all brackets and parenthesis, ignoring the inner ones, but also have the program work in a way to be able to ignore solo ones nested within. While this seems easy on concept, you never know how many will be nested in, along with not knowing if there will ever be a perfect amount of matching pairs at all, requiring a lot of code and testing to get it perfectly right.

This last issue seems easy to fix simply, as all that would need to be done is check for multiple '\n' characters in a row within the brackets and parenthesis. This may be slightly greater than 10 lines, but it is really one solution for brackets that is essentially copy/pasted for parenthesis as well. When looked at in this way, it is definitely 10 lines or less of programming.  