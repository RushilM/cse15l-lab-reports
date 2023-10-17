## Using each command with NO ARGUMENTS

**1. cd**  
```
[user@sahara ~/lecture1]$ cd  
[user@sahara ~]$
```
When using CD with no arugments, the user is returned to the home directory. If the user is already at the home directory, the user stays in the home directory. The working directory in the example above is /home/lecture1 and then becomes /home once cd is used with no arguments.


**2. ls** 
```
[user@sahara ~]$ ls  
Lab1  lecture1  
[user@sahara ~]$
``` 
When using LS with no arguments, the list of files in the current directory is shown. The working directory in this example is /home after the ls command is called, the directory is unchanged.

**3. cat**    
```
[user@sahara ~]$ cat  
editing  
editing  
^C  
[user@sahara ~]$
```
When using cat with no arugments, the user is put into editing mode. User must exit the mode to continue in terminal. The working directory in this example is /home, after cat is called, the working directory is unchanged. When in editing mode the user is able to type into the console, as an example I have typed "editing" above, when enter is pressed the console prints out the input, so "editing" is printed in a line below. This is because CAT doesn't have a file to store the data. In order to exit this mode, ^C (ctrl-C) was used to terminate.

## Using each command with a path to a DIRECTORY as an argument

**1. cd** 
```
[user@sahara ~]$ cd lecture1  
[user@sahara ~/lecture1]$
```
When using cd with a path to a directory as an argument changes the directory to the given directory. In this example we start off in the working director /home, after the command is called the working directory is changed to /home/lecture1.

**2. ls**     
```
*[user@sahara ~]$ cat  
[user@sahara ~]$ ls lecture1  
Hello.class  Hello.java  messages  README  
[user@sahara ~]$*
```    
When using LS with a path to a directory as an argument, the contents of the given directory is listed. The working directory in this example is /home, the working directory is unchanged throughout this example as ls does not change the working directory. 

**3. cat**  
```
*[user@sahara ~]$ cat  
[user@sahara ~]$ cat lecture1  
cat: lecture1: Is a directory*
```   
When using cat with a path to a directory as an argument, the console returns an error because cat cannot be given a directory as an argument. This input returns in an error.   

## Using each command with a path to a FILE as an argument  

**1. cd**  
```
*[user@sahara ~/lecture1]$ cd  
[user@sahara ~]$ cd lecture1/messages/da.txt  
bash: cd: lecture1/messages/da.txt: Not a directory  
[user@sahara ~]$*
```   
When using CD with a path to a file as an arugment, an error is returned as CD required a directory as an arfument. This input returns in an error.  

**2. ls**    
```
*[user@sahara ~]$ ls lecture1/messages/da.txt  
lecture1/messages/da.txt  
[user@sahara ~]$*
```    
When using LS with a path to a file as an argument, filepath is returned.  

**3. cat**     
```
*[user@sahara ~]$ cat lecture1/messages/da.txt  
Hej Verden!  
[user@sahara ~]$*
```     
When using cat with a path to a file as an argument, the contents of the file is resulted. In this case the text file contains the text "Hey Verden!"  



