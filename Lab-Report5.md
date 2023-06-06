# Part 1 – Debugging Scenario


## Student's Post:

Q: What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?

A: I am using a Microsoft Surface computer running Windows 11 in VS Code using git bash.

Q: Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to 
see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.

A: I am seeing an unexpected output when running my bash script. When testing my code in my .sh file, 
my code is passing on the wrong implementation. It passes when I try to divide 1 by 2 which should be .5 
but it returns 0 

Q: Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, 
command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context 
as you can.

A: Here are the my java file, my sh file as well as the command I ran to run the test.sh file:

![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/b863f0fe-e5c8-4491-9969-5b6b9c2e34c5)
![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/3b46b018-0b11-469b-bc01-0ca2cb75a6e2)
![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/205c0c13-aa27-420b-9112-e87b1db34155)


## TA's Response:

Hello there TA Rudy Here, 

Looking at your Test.java file, it seems that your problem resides in your divide method. You will need to change the variable result from an int to a double. Also you will have to typecast the division of x / y into a double. Sicne you updated the content of result into a double you must chnage the method header to support returning a double rather than an integer. 

Here is the updated code:

![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/019a208e-437c-40bc-b9d8-644774d8c72f)

Also, you might want to edit your .sh file to put the actual output as well as the expected output onto a variable to make it simpler to make more tests in the future. This is also be causing an error:

![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/76458eba-f6f6-4f9e-b732-c2e813654a9b)

As you can see, I have updated the code, now when you run the command you previously ran:

![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/b7335ee1-6c2b-45e5-9b6f-8ba9ad6eb9cc)

You no longer pass the test when passing 0 and 1 as parameters. 

# Part 2 – Reflection

Somethings I learned from my time in lab this second half o the quarter than I found really interesting is the use of Vim. When Vim was 
first taught in lecture, I found it really unnecessary to have to relearn how to use the keyboard to write and fix code in Vim. Yet, the more we
worked with Vim in lab and used it conjointly with git in the git bash terminal the more I found its use. I really like how I can fix code directly 
in the terminal and git push the code back onto github without having to spend time looking for the file on github manually. Even though It still 
catches me off guard at times when I can't use the mouse in Vim, I understand why it was intended like this as it is meant to not have to take your 
hands off the keyboard. These last labs, as well as the last Lab Report 4 were some of the most useful lab experience that I am sure it will drastically 
help me later on in future CSE courses. Thank you and all the tutors for your help, y'all are amazing!
