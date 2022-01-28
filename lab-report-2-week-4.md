# Fixing Bugs 

This webpage will be for lab report 2! 

## First Code Change 

![code1](code-change-1.png) 

The file that made me make this change was an [empty file](https://github.com/ajkristanto/markdown-parse/blob/7e2670f006fcf6c9ab1153ffc5ac0c1e4961606f/empty-file.md). 

![fail1](fail-1.png) 

The file has no links to print out so it crashed because the code could not find what it was supposed to be looking for. The code is looking for the content between an opening and closing bracket, however it does not exist in this file hence there is an error. 

The change that I made avoided this problem because before looking for the values between the brackets, it first checks the file if there is a pair of brackets in the first place. If there is, then we know that there will be a link in the file, if it doesn't then we return a statement stating that there are no links in the file. 

This resulted in this output: 

![fix1](fix1.png)

## Second Code Change

![code2](code-change-2.png)

The file that made me make this change was [test file 6](https://github.com/ajkristanto/markdown-parse/blob/7e2670f006fcf6c9ab1153ffc5ac0c1e4961606f/test-file6.md) 

![fail2](fail-2.png)

There wasn't a failure message per se, however the code identified the image as a link. To avoid this happening, I added an if statement in the code that checks if the first index of the line contains a "!". If it does then it is an image and it will be skipped. I got this code from when the group was working on [Hang Liu's bug](https://github.com/HangLiu01/markdown-parse/blob/1ecefe3d1e32cd5c54f991ec3016bc31ef003f8b/MarkdownParse.java). Instead of an else statement from my code in the first code change, I switched it for another if statement that checks if the list is empty then return a statement indicating so. This is to avoid the problem of if the file has both a link and an image. It is also to state that there is no links in the file if there is only an image. 

This resulted in this output: 

![fix2](fix2.png)

## Third Code Change 

![code3](code-change-3.png)

The file that made me make this change was [test file 2](https://github.com/ajkristanto/markdown-parse/blob/7e2670f006fcf6c9ab1153ffc5ac0c1e4961606f/test-file2.md) 

![fail3](fail-3.png)

The failure message just indicates that the string index is out of bounds. It is trying to extract a character that does not exist in the string. To fix this issue, I added an if statement to check that if the remaining of the markdown does not contain an '[' then to break from the while loop. 

This resulted in this output: 

![fix3](fix3.png)
