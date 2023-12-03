# Lab Report 5

## Part 1

## Multiple Errors when running ListExamples.java!

Student: Both tests seem to pass but I am getting 5 errors when run the bash script. Can someone please help? I have provided a screenshot of the output and my code. 

I simply ran the code using test.sh: ```bash test.sh```

![Alt text](Lab5Screenshot1.png)
![Alt text](Lab5Screenshot2.png)
![Alt text](Lab5Screenshot4.png)

TA: Take a look at your code carefully, you have intilaized "result", a new ArrayList on line 14, but keep in mind how scopes work in Java. Ensure that result is initalized within the merge function.

Student: I see what I did wrong, thanks! The tests work now! Here are my changes:
You were right, even though result was intialized on line 14, it was not itialized within the scope of the merge function!
![Alt text](Lab5Screenshot3.png)

## Part 2 - Reflection

I really enjoyed the lab where we practiced being quicker with VIM. I think that allowed us to be creative with our steps and use the shortcuts within VIM to our advantage to get a faster time. Also it helped that we were competing with our lab partner because that helped us learn from each other and use techniques the other person used. I also believe that VIM is used quite often to make quick edits within servers and getting comfortable with the shortcuts is most definetly a useful skill to have. 
