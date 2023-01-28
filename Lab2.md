# Lab Report 2 : Servers and Bugs
---
Hello everyone!!
Today we are going to learn about a local web server and also learn debugging of computer programs. So let's begin 


# Part 1 : String Server

Screenshot of code :

![Image](Code.png)

Description of my code - In this code

Screenshot of using /add-message :

![Image](First_text.png)

In the above screenshot we can see that the url of the webpage is *localhost:4000/add-message?s=Hi%20Prof.%20Politz*. First, my code implements method  url.getpath() and since the path in the above URL contains /add-message so the else statement block gets executed. The query in this url is */add-message?s=Hi%20Prof.%20Politz* Here, according to my code I split the query at "=" sign and then concatenate parameters[1] which is "Hi Prof. Politz" and "\n" (escape sequence for new line) to the empty string called str. My program returns this string and that is what we see on the webpage.

![Image](Second_text.png)

In this second webpage screenshot we can see that the url of the webpage is *localhost:4000/add-message?s=CSE%2015L%20is%20a%20very%20interesting%20course*. Just like the previous case, first my code implements method url.getpath() and since the path in the above URL contains /add-message so the else statement block gets executed. The query in this url is */add-message?s=CSE%2015L%20is%20a%20very%20interesting%20course* Here, according to my code I split the query at "=" sign and then concatenate parameters[1] which is "CSE 15L is a very interesting course" and "\n" (escape sequence for new line) to the variable str which already holds the value "Hi Prof. Politz". My program returns this string and that is what we see on the webpage.




![Image](Final_text.png)
