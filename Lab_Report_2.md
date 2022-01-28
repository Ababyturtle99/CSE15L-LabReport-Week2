
# Lab Report 2: Debugging and Testing

During the lab, there were 3 main bugs that my group had seen and fixed. The files that caused the symptoms to surface are the ones below.

![FailFiles](https://i.ibb.co/TPws7NB/files-that-made-it-fail.png)

When these files are the input for running Markdownparse.java, these are the results.

![FailedRuns](https://i.ibb.co/y8MtBgj/failed-tests.png)

Case 1:

FailFile.md contains image embeds, which should NOT be seen as links, but the program originally copies anything that is within parenthesis after a set of brackets. Image embeds follow the exact format of links, but have a '!' at the front. So, the program does not see the difference between the two as it only checks for the brackets and parenthesis, copying the image embed and printing it as our symptom.


Case 2: 

FailFile2.md contains no links, but does contain a pair of brackets and a pair of parenthesis that exist a far distance away. The program does not check whether the link is a properly formatted link, once again only looking to see if there are parenthesis followed by brackets, copying what is inside the parenthesis, which may not even be an imbed, such as in the file, and printing a non link.


Case 3:

FailFile3 has two links, except one of them does not have their open or closed parenthesis. Since this exact problem also occurs with brackets, I will write as if it's one problem, since it nearly is. Our bug is that when a bracket/parenthesis is not found, the .indexOf function returns -1, and the program still acts as if it found it, which can cause one of two symptoms. For one, the program may infinitely loop if it fails to find anything other than the closed parenthesis, as it returns the -1 to start the next search from. However, it will cause an index out of bounds exception if the last close parenthesis cannot be found, as it will attempt to create a substring with a -1 stopping point.  

Thus, the solutions are presented below in the following picture and explained in words below the picture.

![CodeChanges](https://i.ibb.co/CK7CcS8/correction-to-code.png)

Case 1: For every set of brackets the program finds, it checks if the opening bracket is the start, or if the character before isn't an '!' before continuing. The firt check avoids another issue, an index out of bounds exception in the case that the link is the start of the file, and thus the first opening bracket is index 0.

Case 2: For this, before we make and add the link to the list, we check if the link was actually an embedded link by checking if the closed bracket and open parenthesis are right next to each other, and if they are, the link will be copied into the list.  

Case 3: To fix this issue, we simply add checks after finding each set of brackets and parenthesis, breaking out of the loop if it fails to find any of them, as the file will have no more links if either bracket or parenthesis cannot be found.
