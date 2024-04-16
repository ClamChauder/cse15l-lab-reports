# Lab Report 2 (URLs and Servers)
---
## Remotely Connecting to CSE15L account
Upon using `ssh` to login to the `ieng6` server, I got a message asking to confirm the authenticity of the server and decide whether or not I wanted to continue connecting. After connecting, I noticed the cluster status which I believe displays the three different `ieng6` computers that I could have connected to, as well as the time at which I connected, the number of users connected to each host, and the average CPU load for different time frames.

![Login](/images/sshlogin.png)

---
## Building and Running the Server
To start the lab, I exited the terminal using the `exit` command, and proceeded to `git clone https://github.com/ucsd-cse15l-s24/wavelet` in my local terminal. The two files in the repository were 
`Server.java` which we were told would be explained in the future, and `NumberServer.java`, which manages a single number and uses `Server.java` to create a web server.  
  
Reading through the code in `NumberServer.java`, we determined that the `handleRequest` method takes in a url as a parameter and modifies the web server accordingly. The first `if` statement argument (line 10) checks if there is a `path` or `query` after the `domain`, and if not, then it simply prints the value of the stored number. The next argument checks if the `path` is equal to "increment", increments the stored value by one if it is and prints that the value has been incremented. The last argument checks for the `add` path, splits the `query` that follows it into two string vectors, and checks if the first vector is valid and equals "count". If so, the stored value is increased by the number following the `=`, and the result is printed.
![Login](/images/numberserver.png)

To run the server, I first compiled both files using the `javac` command. I then ran `java NumberServer 3001` which started the server on the port `3001`. Below are the results from testing different paths and queries.

Root path:  
![Root path](/images/rootdir.png)  
  
Increment:  
![Increment](/images/increment.png)  
  
Add:  
![Add](/images/add.png)  
  
Error:  
![Error](/images/error.png)  

---
## Running the Server on a Remote Computer
To run the server on a remote computer, I used `ssh` to log back in to the `ieng6` server, then repeated the process of cloning the repository and compiling the two files in it. My lab partners did the same, and we were able to connect to each other's web servers. Any changes we made by adding or incrementing the value could be seen by everyone, which makes me think the number is stored in the 
`num` variable on the `ieng6` server.

A change I made to the `NumberServer.java` file on my local repository was to have it print my name whenever the root directory path was given. However, this change did not carry over to the repository on the `ieng6` server, because they are separate repositories. One thing that can be done, though, is to create a public github repository that others can edit and clone to the server.

---
## Accessing URLs from the Command Line with curl  
The `curl` command can be used to access URLs, and by default prints out the contents of the URL to the terminal. Below is a screenshot of two terminals side by side, one running the server and the other loading different URLs via `curl`.
![Side by side](/images/sidebyside.png)  

---
## Making the Simplest "Search Engine"  

Back in the local version of the respository, I created a new file called `SearchEngine.java` where I created a web server to keep track of strings, similarly to `NumberSever.java`. It supports paths for printing the list of strings, adding new strings to the list, and searching through the list and returning any strings that contain the given substring. Below is the code for `SearchEngine.java` as well as examples of testing each path.

![Search Engine Code](/images/searchengine.png)

Add:  
![Add](/images/addapple.png)  

Root path (print list):  
![Root path](/images/default2.png)  
  
Search:  
![Search](/images/searchapp.png)  

Similarly to before, you can add words to a list and have others see them. This makes me think that the list of strings is also stored locally in the server host’s variable for the list.
