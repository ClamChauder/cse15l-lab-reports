# Lab Report 2
---
Upon using `ssh` to login to the `ieng6` server, I got a message asking to confirm the authenticity of the server and decide whether or not I wanted to continue connecting. After connecting, I noticed the cluster status which I believe displays the three different `ieng6` computers that I could have connected to, as well as the time at which I connected, the number of users connected to each host, and the average CPU load for different time frames.

![Login](/images/sshlogin.png)

To start the lab, I exited the terminal using the `exit` command, and proceeded to `git clone https://github.com/ucsd-cse15l-s24/wavelet` in my local terminal. The two files in the repository were 
`Server.java` which we were told would be explained in the future, and `NumberServer.java`, which manages a single number and uses `Server.java` to create a web server.  
  
Reading through the code in `NumberServer.java`, we determined that the `handleRequest` method takes in a url as a parameter and modifies the web server accordingly. The first `if` statement argument (line 10) checks if there is a `path` or `query` after the `domain`, and if not, then it simply prints the value of the stored number. The next argument checks if the `path` is equal to "increment", increments the stored value by one if it is and prints that the value has been incremented. The last argument checks for the `add` path, splits the `query` that follows it into two string vectors, and checks if the first vector is valid and equals "count". If so, the stored value is increased by the number following the `=`, and the result is printed.
![Login](/images/numberserver.png)
  
To run the server, I first compiled both files using the `javac` command. I then ran `java NumberServer 3001` which started the server on the port 3001. Below are the results from testing different paths and queries.

Root path:  
![Root path](/images/rootdir.png)  
  
Increment:  
![Increment](/images/increment.png)  
  
Add:  
![Add](/images/add.png)  
  
Error:  
![Error](/images/error.png)  

