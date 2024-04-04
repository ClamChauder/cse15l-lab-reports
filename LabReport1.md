# Lab Report 1 (Week 1)
---  
**The `cd` command:**  
As seen below, the initial absolute path given by the `pwd` command is `/c/Users/bchau/lecture1`. After using the `cd` command, the 
absolute path became `/c/Users/bchau`, and executing it again produced no change to the absolute path which is not an error. This indicates that the `cd` command without arguments changes the current directory to the home directory.
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
---
**The `ls` command**  
Again, the initial absolute path is `/c/Users/bchau/lecture1`. Using `ls` without arguments lists all the directories and files within the current directory, while adding the name of a different directory as an argument lists all the directories and files located in that directory. 
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
**The `cat` command**
---
With no arguments:
Absolute paths: `/c/Users/bchau`, then `/c/Users/bchau/lecture1` after `cd`
```
bchau@MSI MINGW64 ~ (main)
$ cat

bchau@MSI MINGW64 ~ (main)
$ cd lecture1

bchau@MSI MINGW64 ~/lecture1 (main)
$ cat

```
With no arguments, the `cat` command produces no output, and   .......................................................

With a directory as an argument:  
Absolute path: `/c/Users/bchau`
```
bchau@MSI MINGW64 ~ (main)
$ cat lecture1
cat: lecture1: Is a directory
```
Absolute path: `/c/Users/bchau/lecture1`
```
bchau@MSI MINGW64 ~/lecture1 (main)
$ cat lecture1
cat: lecture1: No such file or directory
```
Using the `cat` command with a directory as an argument will indicate whether the argument directory exists inside the current working directory. The `lecture1` directory exists within the home directory, but not within itself, therefore the output makes sense and is not an error.  

With a file as an argument:
Absolute path: `/c/Users/bchau/lecture1`
```
bchau@MSI MINGW64 ~/lecture1 (main)
$ cat Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);
    System.out.println(content);
  }
}
```
Absolute path: `/c/Users/bchau`
```
bchau@MSI MINGW64 ~ (main)
$ cat Hello.java
cat: Hello.java: No such file or directory
```
As seen above, using `cat` with a file as an argument will either indicate that the file does not exist in the current 
working directory, or if it does, it will print the contents of the file. Both outputs are correct.
