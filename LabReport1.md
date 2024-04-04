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

```
bchau@MSI MINGW64 ~ (main)
$ pwd
/c/Users/bchau

bchau@MSI MINGW64 ~ (main)
$ cd lecture1

bchau@MSI MINGW64 ~/lecture1 (main)
$ ls
Hello.java  messages/  README

bchau@MSI MINGW64 ~/lecture1 (main)
$ ls messages
en-us.txt  es-mx.txt  zh-cn.txt

bchau@MSI MINGW64 ~/lecture1 (main)
$ pwd
/c/Users/bchau/lecture1

bchau@MSI MINGW64 ~/lecture1 (main)
$ ls
Hello.java  messages/  README

bchau@MSI MINGW64 ~/lecture1 (main)
$ cd Hello.java
bash: cd: Hello.java: Not a directory

bchau@MSI MINGW64 ~/lecture1 (main)
$ pwd
/c/Users/bchau/lecture1
```
