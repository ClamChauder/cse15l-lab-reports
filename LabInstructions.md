Lab Report 2 - Servers and SSH Keys (Week 3)
As with the first lab report, you'll write this as a Github Pages page, then print that page to PDF and upload to Gradescope. Make sure to use backticks ` around keywords such as commands, file names, paths, etc. to make them show up as code like cd. Lab report 2 is due Wednesday, April 24 by 10pm. There are 3 parts:

Part 1
Write a web server called ChatServer that supports the path and behavior described below. It should keep track of a single string that gets added to by incoming requests. The requests should look like this:

/add-message?s=<string>&user=<string>
The effect of this request is to concatenate the string given after user=, a colon (:), and then the string after s, a newline (\n), and then respond with the entire string so far. That is, it adds a chat message of the form <user>: <message>

So, for example, after

```
/add-message?s=Hello&user=jpolitz
```  
The page should show
  
```
jpolitz: Hello
```  
and after  

```
/add-message?s=How are you&user=yash
```  
the page should show
```
jpolitz: Hello
yash: How are you
```
(Some browsers might show this as `How%20are%20you` with a special character replacing the spaces; don't worry about fixing that for this example. If you want to look it up it has to do with URL encoding, a topic we won't address right now.)

You can assume that the `s=` parameter always comes before the `user=` parameter, and they are always separated by a `&` as shown above.

Show the code for your `ChatServer`, and two screenshots of using `/add-message`.
For each of the two screenshots, answer the followings three questions:

Which methods in your code are called?
What are the relevant arguments to those methods, and the values of any relevant fields of the class?
How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
By values, we mean specific Strings, ints, URIs, and so on. "abc" is a value, 456 is a value, new URI("http://...") is a value, and so on.)

Part 2
Include a screenshot for each of the following:

On the command line of your computer, run ls with the absolute path to the private key for your SSH key for logging into ieng6.
On the command line of the ieng6 machine, run ls with the absolute path to the public key for your SSH key for logging into ieng6 (this is the one you copied to your account on ieng6 using ssh-copy-id, so it should be a path on ieng6's file system).
A terminal interaction where you log into your ieng6 account without being asked for a password.
Part 3
In 2-3 sentences, describe something you learned from lab in week 2 or 3 that you didn't know before.
