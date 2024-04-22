# Lab Report 2 (Week 3)
[LAB INSTRUCTIONS](https://clamchauder.github.io/cse15l-lab-reports/LabInstructions.html)

---

## Part 1
Chat Server code:  
![Chat Server](/images/Lab2/chatserver.png)


Examples of using `/add-message`:

![Add Jpolitz](/images/Lab2/addjpolitz.png)
1) Relevant Methods and their Arguments:
   - `handleRequest`: The relevant argument for this method is `url`, which takes on the value of `http://localhost:3001/add-message?s=Hello&user=jpolitz`.
   - `main`: Takes in a string array `args` which takes the value of 3001.
   - `handle`: The relevant argument is `exchange` which is an instance of the `HttpExchange` class.
   - `start`: The relevant arguments are `port` and `handler` which are an integer (3001) and a URLHandler object respectively.
   - `ServerHttpHandler`:  The relevant argument for this method is `handler`, which is a URLHandler object.  
2) The  `str` variable inside the `Handler` class is empty at first, and then changes to contain `"jpolitz: Hello"`.

![Add Yash](/images/Lab2/addyash.png)
1) Relevant Methods and their Arguments:
   - `handleRequest`: The relevant argument for this method is `url`, which takes on the value of `http://localhost:3001/add-message?s=Hello&user=jpolitz`.
   - `main`: Takes in a string array `args` which takes the value of 3001.
   - `handle`: The relevant argument is `exchange` which is an instance of the `HttpExchange` class.
   - `start`: The relevant arguments are `port` and `handler` which are an integer (3001) and a URLHandler object respectively.
   - `ServerHttpHandler`:  The relevant argument for this method is `handler`, which is a URLHandler object.  
2) The  `str` variable initially contains `"jpolitz: Hello"`, and after the request it contains
```
jpolitz: Hello
yash: How are you
```
---  
## Part 2

Private key on local machine:

![ls private](/images/Lab2/lsid.png)  
Public key on remote machine:

![ls pub](/images/Lab2/lspub.png)  
Logging in without password:

![No pass](/images/Lab2/nopwd.png)
---  
## Part 3

I learned how to start my own local server, using the java command with a port in a local terminal as well as a remote one. You can display contents of a link to the terminal or save its contents to another file with the curl command.
