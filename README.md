# Custom Programming Language

## Overview

**SAD** is a custom programming language implemented entirely in SmallTalk and compiling to C. The project explores the core principles of designing a programming language. 

This project makes a strong example of systems thinking, principles of programming languages, and object oriented design.

## Features

- Custom syntax and grammar. (Ohm was used for the grammar)
- Parser, interpreter, and Code Generator for executing programs written in the language.
- Fully OOP implementation. 99% of the code base is written in less than 8 lines in a method.
- A pretty printer, formatting the code in a click of a button!
- A symantic analyzer for catching errors.
- If statements, Variables, Functions, Procedures (no returning), and loops.

## Example

The following code will generate C code.

SAD program:
```
sadness 
	reasons
		fact6 isa integer
	sorrows
		disfunction factorial(n isa integer) isa integer
		do
			if n = 0 then
				factorial <- 1
			else
				factorial <- n * factorial(n - 1)
	do
		:-(
			fact6 <- factorial(6)
			writeString "factorial 6 is "
			writeInteger fact6
			writeNewLine
		)-:
```

Generates the following C code:

```
#include <stdio.h>
int fact6;
int _factorial(int n)
{
    int factorial;
    if(n == 0)
        factorial = 1;
    else 
        factorial = n * factorial(n - 1);

    return factorial;
}

int main(int argc, char *argv[]){

    fact6 = factorial(6);

    printf("%s", factorial 6 is );
    printf("%d", fact6);
    printf("\n");

}
```

Which then would be compiled with which ever compiler you choose.

## Running the Program

### Requirements
To test the language you will need a SmallTalk environment. I choose Squeak.
- https://squeak.org/downloads/

### Setup
1. Clone this repo.
2. Open the Smalltalk environment.
3. File-in this repo's src.
4. Run the test cases!

## Why I built this?

This was my final project for my Principles of Programming languages class. With this being said, I went above and beyond in our interpretation because I really enjoyed the systems level and object oriented approach.
