02_Cpp
======

Intro to C++, learning to do things you can already do in Java

Reading
=======

**C++ Programming** at WikiBooks.

All of the readings are free online, though note that the book is under constant revision. If something looks crazy, ask me about it.

I will lecture about this material in class. These readings are meant to be used in reviewing/studying.

1. Why our code is split into .h files and .cpp files: https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/File_Organization (6p)
2. What is the :: operator for? https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Scope Stop at "unnamed namespace"
3. What does the compiler do? What does it NOT do? What does the pre-processor do? What does the linker do? https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Compiler Stop at "Compile speed" (4p) https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Compiler/Preprocessor (13p) https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Compiler/Linker (4p)
4. Bitwise operators. https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#Bitwise_operators (2p)
5. Arrays, and the subscript operator. https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#Subscript_operator_.5B_.5D (5p)
6. Pointers. https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#address-of_operator_.26 and https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#Pointers.2C_Operator_.2A (9p) Skip the part about multi-dimensional arrays, and the part about pointers to functions.
7. Dynamic memory allocation. https://en.wikibooks.org/wiki/C%2B%2B_Programming/Programming_Languages/C%2B%2B/Code/Statements/Variables/Operators#Dynamic_memory_allocation (4p)

Homework
========

1. Fork this repo
3. Fill in the blanks in the main.cpp with code that produces the correct result. Read the comments to find out what they ought to do.
4. Be sure to `git commit` and `git push` often
5. Update this file with your documentation and the answers to questions.
6. When you are ready to turn in your homework, submit a pull request from your repo to mine.
7. Be sure to check the pull requests for my repo on github to make sure it worked, and that your work has been submitted.

Documentation
=========

For each of the following functions in main.cpp, tell me whether or not you think it is working in your submission.

1. prime - Success!
2. defix - Success!
3. sumSlice - Success!
4. square - TODO
5. listPrimes - TODO

Questions
=======

#### 1. In C++, the compiler compiles each .cpp file separately, without looking at the others. Explain why this leads to the need for .h files.  
 - .Cpp files sometimes require other files to run properly, whether it be to run a function or provide other data.  Even though you can put the calls to other .cpp files at the top of each file, .h files are an efficient way to import other .cpp files and have a compiler understand what everything is in each individual .cpp file.

#### 2. Explain the individual roles of the preprocessor, the compiler, and the linker. What type of inputs do they take? What kind of outputs do they produce? What is the purpose of each?
 - The preprocessor replaces any import statements with the code it links to.  The compile then compiles the new, modified code that has the imported code into code that is executable by the machine.  The linker is in charge of all the different .cpp and .h files the current file is linked to, making sure functions called from other files are properly linked to.

#### 3. What is a "pointer"?
 - A pointer is not a variable that holds useful data.  A pointer holds the address of the variable or object we are trying to reach in memory.

#### 4. If I have a variable declared as `int x`, how do I find out what memory address that variable is stored at?
 - To find the memory address of a variable, use the character '&' in front of the variable name, in this case "&x"

#### 5. If I want a variable `p` that can store the address of an int, what type should I declare `p` to be?
 - To hold the address of an int, declare a variable, in this case "p", as "int* p".

#### 6. Just like Java, C++ has a `new` command. But C++ also has a `delete` command that Java does not have. Why do we need `delete` in C++, but not in Java? What is `delete` good for?
 - Java is a lot better at implicitly getting rid of data that is no longer used or important.  C++ does not implicitly get rid of data or overwrite it nearly as well.  Instead, data from C++ can be accessed even after it's life in the code is over if it has not been 'deleted' explicitly.  

#### 7. What is one question about C++ that you would like me to explain in class?
 - How come we need to use "std::cout" in our code or it won't compile, but in some code online, and a class I took in high school, we could compile and run perfectly fun without the "std::"?