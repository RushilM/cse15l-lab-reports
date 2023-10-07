## Using each command with NO ARGUMENTS

**1. cd**  
*[user@sahara ~]$ cd lecture1  
[user@sahara ~/lecture1]$ cd  
[user@sahara ~]$*  
When using CD with no arugments, the user is returned to the home directory. If the user is already at the home directory, the user stays in the home directory.

**2. ls**    
*[user@sahara ~]$ ls  
Lab1  lecture1  
[user@sahara ~]$*    
When using LS with no arugments, the list of files in the current directory is shown  

**3. cat**    
*[user@sahara ~]$ cat  
editing  
editing  
^C  
[user@sahara ~]$*   
When using cat with no arugments, the user is put into editing mode. User must exit the mode to continue in terminal  

## Using each command with a path to a DIRECTORY as an agrgument

**1. cd**  
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ 
When using cd with a path to a directory as an argument cahanges the directory to the given directory

**2. ls**    
[user@sahara ~]$ cat
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
[user@sahara ~]$ 
When using LS with a path to a directory as an argument, the contents of the given directory is listed.

**3. cat**    
[user@sahara ~]$ cat
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory 
When using cat with a path to a directory as an argument, the console returns an error because cat cannot be given a directory as an argument. 





