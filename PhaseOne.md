# Technical Documentation for Binary Code Obfuscation/Anti-Reverse Engineering

## Introduction
In this project we will be utilizing Tigress to obfuscate a simple C program. We will use the flatten and variable renaming transformations in tigress to evaluate their effectiveness in enhancing code security while also testing the performance impact they have. After obfuscating our code, we will be using Ghidra to reverse engineer the codes, seeing how secure they are against these attacks.

## Objective One: Evaluate the Effectiveness of Obfuscation Techniques
-----

## Tigress
**Step 1:**
Download Tigress, there are two download options available- GitHub or the Tigress website, we will be using the website.

**Step 2:**
Extract the Tigress zip file.

**Step 3:**
Navigate to the Tigress directory using *cd usr/local/bin/tigresspkg*

**Step 4:**
Verify that Tigress is downloaded by checking the version using *tigress --version*

**Step 5:**
Now that tigress is installed, transformations are able to be applied to the code. To flatten the code use the command *tigress --Transform=Flatten --Functions=main,sum sum.c --
out=flatten.c*
To rename the variables in the code use the command *tigress --Transform=CleanUp --CleanUpKinds=names sum.c --out=renamed.c*

-----

## Ghidra 
**Step 1:**
Download JDK 21 for your specific system and archeticture.

**Step 2:**
Download Ghidra from the NSA GitHub repository.

**Step 3:**
Extract the contents of the Ghidra zip file.

**Step 4:**
In the terminal, navigate to Ghidra using the command cd *ghidra_11.1.2_PUBLIC*

**Step 5:**
Run Ghidra using the command *./ghidraRun*, Ghidra will automatically open. 

**Step 6:**
Import the compiled C files and analyze them.

-----

## Analysis
From objective one in our project, we analyzed two different types of obfuscated code by using the *time* Linux command to see their performance speed and Ghidra, from these tests we have determined that the obfuscation enhances the security of out C program, but slows down the program up to 4x as much. We determined that it is essential to have a healthy balance between performance impact and security. The two different obfuscation tranformations we tested in Tigress (flattening and variable renaming) both significantly altered our code, but we saw that flattening was more effective in obfuscating as it changes the control form of the program, instead of just the variable and function names. 
