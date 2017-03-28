Author: Zhizhou Zhang
CS255 Project LLVM

Main Idea:
    the main idea of this project is to count the number of dynamic instruction of a given function.
  	To finish the task, we need to insert an instrumentation code into the program at compile
  	time, which is shown on the second function. By linking with origianl excutable, we could
  	count the number on the fly at run-time.

Implementation:
	by using the function provided in .c file, initialize the counter variable, then traversal
	the function by two nested iterator. During the iteration, increase the counter by call 
	increase function and at the end, print out the result

Result:
	Total instructions executed: 1
	Enter the string :cs255
	Reverse string is :552sc
	Total instructions executed: 96

and the static result goes:
	Function: main
		No. 0bb: 12 statements.
		No. 1bb: 4 statements.
		No. 2bb: 25 statements.
		No. 3bb: 3 statements.

	we can see that the actually excuted code used more instructions.