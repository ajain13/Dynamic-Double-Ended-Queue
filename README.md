#Dynamic Double Ended Queue (a.k.a Deque)

A macro implemented “template” for a double-ended queue container,
known as a deque.
The Deque is implemented as a circular, dynamic array.
The following is the way to create a Deque of integer type which can be
used in your code:

```
Deque_DEFINE(int)
```

This will basically result in a text replacement where
Deque_DEFINE(int) will be replace the code for Deque of type integer.

In this case , the struct for the container of int variables would be named, 
```
	Deque_int
```

##REQUIREMENTS :
```
	gcc/g++ version 4.2.1 or up. Preferable 5.2.0.
```


##INSTRUCTIONS TO COMPILE :

1. To compile the mytest.cpp which basically shows the usage of the Deque.hpp file , compile as follows :

			g++ mytest.cpp -o test -std=c++11 -ldl

2. To run ,

		    ./test

3. To use the Deque.hpp for your code , I would recommend you to go through the mytest.cpp file to understand the 
   usage of the Deque.hpp.


##DATA STRUCTURE USED

The data structure used for this project was : Circular Dynamic Array


##SOME OTHER NOTES :

1. The code does not completely take care of memory leaks.

2. To test for memory leaks , use the following command(assuming valgrind is installed) :
```
	valgrind --tool=memcheck --leak-check=yes ./test
```
(or)
```
	valgrind --tool=memcheck --leak-check=yes --show-reachable=yes --num-callers=20 --track-fds=yes ./test
```
3. Before running with valgrind , reduce the number of iterations in the performance test code block of mytest.cpp which will make
   the execution complete early.
