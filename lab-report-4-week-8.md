# Week 8 Lab Report


## Snippet 1

To decide which is the real links, I used the [CommonMark demo site](https://spec.commonmark.org/dingus/). 

![Snippet1](snip1-1.png)
![Snippet1](snip1-2.png)

From the website, I decided that the wanted links would be what is referred to as an href in the HTML. Hence the links would be: "%60google.com", "google.com", "ucsd.edu". However, since "%60" is invalid for a link, I just changed it to "google.com" when testing. 

From my own implementation: 

![S1-Mine-Code](snip1-test-me.png)

Then this is the result: 

![S1-Mine-Result](snip1-test-me-r.png)


It didn't pass because the `assertEquals` was not equal on Line 61. This is because the expected output and the actual output differs. My code takes url.com as a link and also take the ` in google.com as a link eventhough they are both invalid. 

For the implementation I reviewed: 

![S1-Rev-Code](snip1-test-rev.png)

Then this is the result: 

![S1-Rev-Result](snip1-test-rev-r.png)


It also didn't pass because the assertEquals was not equal. This code also considers url.com as an output and also has the `google.com as an output. However, it does not have ucsd.edu as an output. 

Hence, to avoid this problem in my own code we must change the code. So we could do this by checking if there is a backtick that opens and closes. So check if theres two backticks. We need to check if it opens before [ and closes before ]. If it exists, skip over it because the backticks will make it a codeblock and not a link. If the backtick is inside the url, ignore it because it is not a valid input for a url. We can do this by making an if statement that checks if there is a backtick before the square brackets close. This will solve the url.com problem. Then we can add another if statement once it goes into pulling the url content and check if there is an invalid component such as the backtick, punctuations and so on then to ignore the component. This should fix the "`google.com" output. 
