# Lab Report 1
---

## cd:
**No Arguments**
```
[user@sahara ~]$ cd
[user@sahara ~]$
```
Working Directory: /home
Explanation: Because there was no argument, there is no change in the directory. Therefore it stays in the default directory.
Not an error.


**Directory as an Argument**
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
Working Directory: /home
Explanation: The command changes the directory to the directory put in as an argument.
Not an error.


**File as an Argument**
```
[user@sahara ~/lecture1/messages]$ cd en-us.txt 
bash: cd: en-us.txt: Not a directory
```
Working Directory: /messages
Explanation: 
Error. 


## ls:
**No Arguments**
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
```
Working Directory: /lecture1
Explanation: 
Not an error.


**Directory as an Argument**
```
[user@sahara ~/lecture1]$ ls messages/
en-us.txt  es-mx.txt  ja.txt  zh-cn.txt
```
Working Directory: /home
Explanation: 
Not an error.


**File as an Argument**
```
[user@sahara ~/lecture1]$ ls README 
README
```
Working Directory: /lecture1
Explanation: 
Not an error. 


## cat:
**No Arguments**
```
[user@sahara ~]$ cat

```
Working Directory: /home
Explanation: 
Not an error.


**Directory as an Argument**
```
[user@sahara ~]$ cat lecture1/
cat: lecture1/: Is a directory
```
Working Directory: /home
Explanation: 
Error.


**File as an Argument**
```
[user@sahara ~/lecture1]$ cat README 
To use this program:

javac Hello.java
java Hello messages/en-us.txt
```
Working Directory: /lecture1
Explanation: 
Not an error. 
