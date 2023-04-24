# Part 1
* Here is a screenshot of my code for StringServer:
![Image](stringServer.png)
* And below are two screenshots using /add-message twice:
![Image](localHost1.png)
* In the image above, I am calling /add-message for the first time.
* The handleRequest method is called. When this is called, the String value str at first equals "", and the argument being passed is /add-message?s=hello
* Because /add-message is conatined in the url, "hello" and a line break are added into str, and the message "hello" is printed on the site.
![Image](localHost2.png)
* In the image above, I am calling /add-message for the second time.
* The handleRequest method is called. When this is called, str equals "hello" + "\n", and the argument being passed is /add-message?s=thanks
* Because /add-message is contained in the url, "thanks" and a line break are added into str, and the message "thanks" is printed on the site below the first message.

# Part 2
* Here is code with two methods that attempt to reverse the order of items in an array:
