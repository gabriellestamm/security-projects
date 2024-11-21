# Binary Code Obfuscation/Anti-Reverse Engineering
## Phase Three

---

# Project Overview
In this project we are testing 14 different obfuscation techniques through Tigress to determine the most effective obfuscation technique on a simple C program. We are doing this to compare these different obfuscation techniques to see which of them are the most effective while not significantly hindering performance impact. 

---

# Obfuscation
Obfuscation is the act of altering a program to where no identifying traits are visible. This can be used for code protection for anti-reverse engineering, but obfuscation can also be used on malware, helping it bypass virus scanners.

![An-example-of-randomization-obfuscation](https://github.com/user-attachments/assets/3d145273-4505-4a07-9872-3d0456a1e87f)

The photo above has been derived from (https://www.researchgate.net/publication/279861980_JSObfusDetector_A_binary_PSO-based_one-class_classifier_ensemble_to_detect_obfuscated_JavaScript_code)


# Objectives
## Evaluate the Effectiveness of Obfuscation Techniques
### Implement Obfuscation Techniques Using Tigress​

We will be using 14 obfuscation techniques on the same, simple C program using Tigress. 



### Analyze the Performance Impact ​

We will be analyzing the performance impact (binary size increase & execution time increase) for each of these obfuscation techniques and comparing them to the original, unobfuscated C program. 

### Assess Obfuscation Strength 

We will be assessing the strength of each of these obfuscation methods based on the previously mentioned metrics. 

## Compare and Evaluate Practicality of Obfuscation Techniques ​

### Develop and Execute Test Cases for Reverse Engineering​

We are going to be developing and executing two test cases on each of the obfuscated programs.

### Document the Obfuscation Process and Results​

Our obfuscation process and results will be documented for future reference.

### Compare with Existing Literature ​

We have 8 papers written on similar topics, to which we will be comparing and finding any gaps in. 

---

# Process

This flowchart showcases our process for obfuscating our code. 

![csc466](https://github.com/user-attachments/assets/3c541cda-8b97-48ac-bb86-9203ca36700b)


# Environment Setup

This project was executed on a controlled Kali Linux VM. We used the most recently updated versions of Tigress and Ghidra for obfuscating and reverse engineering.

--- 

# Obfuscation Techniques Used

- Flattening
- Renaming
- Bogus Function Virtualization
- Opaque Bogus Function
- Bogus Output Generation
- Bogus Function Types
- Virtualization Transform
- Virtualize Short Identifiers
- Pointer Stack
- Indexed Stack
- Virtualize Optimize Body
- Virtualize Trace
- Virtualize Tagged Store
- Virtualize Stack Size
- VIrtualize Dump
- Virtualize Conditional Kinds

  ---

  # Test Cases
  ### Binary Size Increase Percent
  
  ![binary](https://github.com/user-attachments/assets/9bda582e-aca2-4570-b865-281bd2f2ea5f)
  As seen in this graph Virtualization, Polymorphic Virtualization, and Flatten all had a high binary size increase, whereas Short Identifiers, Optimize Control Body, and Tagged Store all had a low increase.

### Execution Time Increase

![exec](https://github.com/user-attachments/assets/fc5b7cb0-6187-464c-81be-42d62886267d)
  As seen in this graph, similar techniques that also had a higher binary size increase also had a longer execution time and vice versa.

---

# Comparison with Literature
We used 8 pieces of literature for this project, where we found that none of them used Tigress as their obfuscator. Our use of Tigress helps to fill in that gap and provide more insight on different kinds of obfuscation techniques. 

--- 

# Conclusion
In conclusion, this project covers a range of obfuscation techniques, testing each of them for execution time speed and binary size increase, to see which obfuscation techniques are the most helpful in safeguarding code while still not limiting performance speed. We saw that certain obfuscation techniques, such as virtualization, result in a large hit on performance, while others, such as short identifiers do not. Obfuscating software programs plays a big role in software engineering and cybersecurity, limiting reverse engineering attemps and attacks. 
