Vim Lab Report!

Log onto your ieng6 account (Step 4):

Keys typed: 
 
```
 ssh <Space> cs15lsp23sb@ieng6.edu (.ucsd after ieng6 if needed), <Enter> .
```
          
Example:

![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/dae36cc4-6729-439a-936e-bc8a7ed27e10)

For this step, I opened a git bash terminal and logged into my personal ieng6 account we been using for this course


Git clone repository from lab onto ieng6 account (Step 5):

Keys typed: 

```
 git <Space> clone <Space> https://github.com/ucsd-cse15l-s23/lab7 <Enter>
```

Example:

![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/390b33b8-fc95-49af-82ea-844439a8ce92)

For this step, once I am inside my ieng6 account, I clone the repository given in step 4 of this week's lab


Run and demonstrate tests failing (Step 6):

Keys typed: 

```
 ls <Enter>
 cd <Space> lab7
 ls <Enter>
 javac <Space> -cp <Space> .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar <Space> *.java <Enter>
 java <Space> -cp <Space> .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar <Space> org.junit.runner.JUnitCore <Space> ListExamplesTests <Enter>
```

Example:

![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/3d6c9692-0105-4ce0-9fc0-4b7cdd509def)
![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/cefcf4ec-6872-41fe-ae37-1887d8092cf2)

For this step, after cloning the repository I used ls to see what folders there are available, then I change my directory (cd) to Lab7 since this is were the listExamples code as well as the tester file. I ls to check the name of these files exactly and then compiled and ran the code based on the way we do it on a Mac (bash uses the mac version instead of the windows version to get this desired output)

Fix the failing test in ListExamples.java (Step 7):

Keys typed: 

```
vim <Space> ListExamples.java <Enter>
</> index1 <Enter> <n> <n> <n> <n> <n> <n> <n> <n> <n> <l> <l> <l> <l> <l> <l> <a> <Backspace> 2 <Esc> 
```

Example:

![image](https://github.com/Ruuudy1/cse15l-lab-reports/assets/130013367/2b2bd98e-e07c-46c4-84ba-738923aec52b)


For this step, 


Run and demonstrate tests now succeding (Step 8):

Commit and push changes to Github (Step 9):
