# COSC 2306 - Data Programming 
## Assignment - 0 ##

### Due Date: Feb. 7, 2022 11:59 PM ###

#### The goal of this assignment is to become familiar with development using an IDE, working with git for code management, and to practice with basic data types in Python.  ####

In this assignment, you are developing a simple ciphering system that takes any message as input and produces a ciphered message as output. 

In doing so, you have to write functions to perform reading and writing of messages using file operations and write functions for generating a cipher code and ciphering input messages.
All functions for file operations are to be written in **fileio.py** and functions for ciphering in **cipher.py**.

Messages to be ciphered and the ciphercode is to be read by your program from input files.
The ciphercode is provided in a text file which will have the following structure:

    - K: This is just a test
    - V: Line two is new to m
**K:** indicates the key of the cipher code while **V:** indicates the associated value.  
In this simple cipher code, each character in the key maps to a corresponding character in value, 
where the correspondence is based on sequential ordering.  
In the above example, the letter **T** is mapped to letter **L**, **h** to **i**, **i** to **n**, **s** to **e**, and so on.
1. You are to write a file operation function `read_keyvalue(filename)` that reads the file with the ciphercode and 
generates two lists of single-character strings, one from the key line and another from value line.
2. You are to write ciphering operations to include the function `make_dictionary(l1, l2)` that takes two equal-length lists 
of single-character strings. It creates and returns a dictionary using the elements of l1 as keys and the elements of l2 as values. 
3. Another ciphering operation and corresponding function to write is `cipher(s, d)`.  The parameter s is a string and d is the dictionary created by `make_dictionary`. 
Function cipher(s, d) uses dictionary d to replace characters in s that are keys in d with the corresponding key value. 
Characters in s that are not dictionary keys are left unchanged in the ciphered version of the string s. 
The ciphered string is returned. 
4. The string s is to be read from an input file.  This should be accomplished by a function `read_message(filename)` 
as part of file operations, which should open the input file and read all lines in the file treating each 
line as the input message to be ciphered.  Each line read should be used as s in the function `cipher(s, d)`.
5. Each ciphered message returned by the function `cipher(s, d)` should be written to an outfile file.  
To do so, you are to write the function `write_ciphered_messages(ciphered_message, filename)` where 
ciphered_message is the string returned by `cipher(s, d)` and filename is the name of the file where 
ciphered messages are written.

All code for file operations is to be implemented in the file **fileio.py**.  
All code for ciphering operations is to be implemented in the file **cipher.py**.

You are already provided with the files and template function definitions.  
Make sure to add comments to your program. 
You are also given code with the main program in file **pr_01.py**.  This includes all function calls and implements the ciphering system.

**Note:**
   
  - Please do not change the code structure.
  - Usage:
   
        - python pr_01.py -kv <ciphercode file> -m <input messages file>
        - Example: python pr_01.py -kv input/ciphercode.txt -m input/messages.txt
  - Please make sure the code runs when you run the above command from prompt/terminal
  - All the output files are saved to "output/" folder

A file with ciphercode (ciphercode.txt) and a file with input messages (messages.txt) are 
provided for testing: input\ciphercode.txt and input\messages.txt.<br>

**PS. Please do not change: pr_01.py, requirements.txt, and Jenkinsfile.**


-----------------------

<sub><sup>
License: Property of Quantitative Imaging Laboratory (QIL), Department of Computer Science, University of Houston. This software is property of the QIL, and should not be distributed, reproduced, or shared online, without the permission of the author This software is intended to be used by students of the Data Programming course offered at University of Houston. The contents are not to be reproduced and shared with anyone with out the permission of the author. The contents are not to be posted on any online public hosting websites without the permission of the author. The software is cloned and is available to the students for the duration of the course. At the end of the semester, the Github organization is reset and hence all the existing repositories are reset/deleted, to accommodate the next batch of students.
</sub></sup>


