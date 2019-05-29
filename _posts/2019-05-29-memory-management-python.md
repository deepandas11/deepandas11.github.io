---
layout: post
title:  "Python Memory Management"
categories: Python
---

This is mostly a compilation of some of the mose crucial concepts that I grasped while studying rapidly about the said topic. I stumbled upon this while doing a project of my own. 

## The Characters 
The way I look at it, Python invloves a few characters in this Memory management scheme: The first and the most obvious one being the **Memory** itself, almost analagous to a book with fixed size pages. Several **writers**, or the applications and processes on the system, can now use this book to write their own stuff on it. Some of the stuff written long back are not relevant and so, they have to be removed by the **garbage collector**.


## CPython 

Memory management is nothing but the process by which applications read and write data. Since there's only a finite amount of storage space available at any given time, the process responsible for allocating these resources has to be optimized. This process of providing memory is generally called **allocation**.

One thing to keep in mind is that a Python program goes through several layers of abstraction before it actually interacts with the hardware. That's one of the flip sides for it being a high level language. One of the layers that the program interacts with before reaching the hardware is the Operating System. Memory management for Python code is handled by the Default Python application installed in the Operating system, called **CPython**. No points for guessing. It's actually written in C. 

So, what does this Default Python implementation written in C, actually do?: It basically achieves two main tasks:

- Interpret written code based on the rules referenced in the reference manual. This is essentially the step where your Python code is interpreted into bytecode. This bytecode is actually saved in the ```.pyc``` or ```__pycache__``` folder. 
- Execute this interpreted bytecode on a virtual machine.

CPython has a few limitations as well. Firstly, it is written in C and therefore, has no Object Oriented features. To imitate Python's universal object implementation, CPython creates a struct called ```PyObject```, which every other object in CPython uses. This ```PyObject``` contains two things:
- ```ob_refcnt```: Reference Count
- ```ob_type```: Pointer to another type

*TLDR: CPython(aka the Default Python Implementation) sits in your OS and achieves the task of executing your Python code. This is also where the Memory management algorithms and structures exist.*







```python
import numpy as np 

a = np.ndarray([1,2,3])


print(a)
```


### Next

In this section, we will check both inline \\( a = x^2 + y^2 \\) and block Latex Equations using MathJax

\\[ b = x^2 + y^2 \\]

\\[ b = \frac{1}{n^2}\\]

We are done!

