## Lab Report 3 - Bugs and Commands (Week 5)
## Part 2

The default grep command takes in two arguments-a string and a file name-and returns any instances of that string within the file. There are also variations of this command that have different behaviors and return different outputs, such as `grep -w`, `grep -r`, `grep -l`, and `grep -c`, to name a few. The mentioned variants are discussed below.

`grep -w`
The 'w' stands for "word, and using this variation will return any instances of the whole word within the file, excluding any words that may include this string as a substring. It could be useful for situations in which you are looking for a certain bit of information, but can't remember anything about it except for a few words

![Grep -r](images/Lab3/grepw.png)
