# Lab Report 1 (Week 1)
---  
**The `cd` command:**  
As seen below, the initial absolute path given by the `pwd` command is `/c/Users/bchau/lecture1`. After using the `cd` command, the 
absolute path became `/c/Users/bchau`, and executing it again produced no change to the absolute path. This indicates that the `cd` command without arguments 
changes the current directory to the home directory.
```
bchau@MSI MINGW64 ~/lecture1 (main)
$ pwd
/c/Users/bchau/lecture1

bchau@MSI MINGW64 ~/lecture1 (main)
$ cd

bchau@MSI MINGW64 ~ (main)
$ pwd
/c/Users/bchau

bchau@MSI MINGW64 ~ (main)
$ cd

bchau@MSI MINGW64 ~ (main)
$ pwd
/c/Users/bchau
```  
Below, the initial absolute path is the home directory, and after using `cd lecture1` it changes to `/c/Users/bchau/lecture1`. 
From there, trying to `cd` to the file `Hello.java` yields the output `bash: cd: Hello.java: Not a directory`. This is not an error, because `cd` stands for 
"change directory," and a file is not a directory.
```
bchau@MSI MINGW64 ~ (main)
$ pwd
/c/Users/bchau

bchau@MSI MINGW64 ~ (main)
$ cd lecture1

bchau@MSI MINGW64 ~/lecture1 (main)
$ pwd
/c/Users/bchau/lecture1

bchau@MSI MINGW64 ~/lecture1 (main)
$ cd Hello.java
bash: cd: Hello.java: Not a directory

```
**The `ls` command**  
Again, the initial absolute path is `/c/Users/bchau/lecture1`. Using `ls` without arguments lists all the directories and files within the current directory,
while adding the name of a different directory as an argument lists all the directories and files located in that directory. 
Finally, using a file name as an argument simply returns the name of the file. None of these outputs are errors.
```
bchau@MSI MINGW64 ~/lecture1 (main)
$ ls
Hello.java  messages/  README

bchau@MSI MINGW64 ~/lecture1 (main)
$ ls messages
en-us.txt  es-mx.txt  zh-cn.txt

bchau@MSI MINGW64 ~/lecture1 (main)
$ ls Hello.java
Hello.java
```
