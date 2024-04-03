# Lab Report 1 (Week 1)
---  
**The `cd` command:**  

Using `cd` without arguments  
```
bchau@MSI MINGW64 ~/lecture1 (main)
$ cd

bchau@MSI MINGW64 ~ (main)
$ cd

bchau@MSI MINGW64 ~ (main)
$ cd

```  
Initially, the absolute path given by the `pwd` command was `/c/Users/bchau/lecture1`. After using the `cd` command, the 
absolute path became `/c/Users/bchau`, and executing it again produced no change. The output
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
Using `cd` with an argument  
```
bchau@MSI MINGW64 ~ (main)
$ cd lecture1

```
*Produces no output, but changes the cwd*


```
bchau@MSI MINGW64 ~/lecture1 (main)
$ cd Hello.java
bash: cd: Hello.java: Not a directory
```
