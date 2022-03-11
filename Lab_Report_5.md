# Lab Report 5

In order to find the tests that differed, I copied the echos of the loop into results files and used vimdiff to find the differences. It clearly highlights tests that differ, and made it really easy to do this part of the assignment. The two tests that differed were files 32 and 41, with these results. The left side is the provided code's results while the right side is my code. 


32

[]  |  [/f&ouml;&ouml; "f&ouml;&ouml;"]

mine(right) is correct, since the preview shows that the link embeds within VSC.

41

[] | [url &quot;tit&quot;]

mine(right) is incorrect, as my program identified the test as a proper link embed, while the preview shows otherwise.

To start with 32, the problem with the provided code is that it checks for spaces within the link to invalidate the embed, however the preview shows that links can clearly exist with spaces in them, and the program would require more checks to find whether the .md link is correct or not.

![providedCode](https://i.ibb.co/PcqpB6Q/fix-this-area-too.jpg)

However, my code isn't any better, because while the provided code doesn't fully check all things that invalidate it as a link, mine does not check any text within the link URL to see if it invalidates it and is not a proper embed. Clearly to fix this, I would just need to add these if statements and check for the things that may make the embed fail within the text of the URL.

![myCode](https://i.ibb.co/4mWczZx/fix-this-area.jpg)