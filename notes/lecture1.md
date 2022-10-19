Some features of C include:
* Structures, union - compound datatypes
* Pointers - memory, arrays
* External Standard Libraries - I/O, etc
* Macro preprocessor

Some uses of C:
* OSes
* Mircocontrollers: automible and airplanes
* Embedded processors
* DSP processors

C lacks:
* Exceptions
* Range checking
* Garbage collection
* Object-oreinted programming
* Polymorphism

Things to be careful about with C:
* No range checking
* Limited type safety at complie time
* No type checking at runtime

Note:
* Always run a debugger like gdb 
* Never run as root


GCC -> complier 
example: gcc -Wall infilename.c -o outfilename.o


Some useful gdb commands
* break linenumber      -> create breakpoint at specified line 
* break file:linenumber -> create breakpoint at line in file
* run -> run program
* c  -> continue execution 
* next  -> execute next line             
* step -> execute next line or step into function
* quit -> quit gdb etc.


Structure of a .c file 
#==============================

/* Begin with a comment about file contents */

 Insert #include statements and preprocessor definitions

 Function prototype and variable declarations

 Define main() function {
    Function body
 }

Define other  function {
    Function body
 }

#==============================


The #include macro
 Header files: 
  * includes constants, functions, etc

  #includes <stdio.h> -> Reads the contents of the header file stdio.h
  stdio.h:
   * includes basic I/O facilities.
   * is part of the standard C library (other important headers include: ctype.h, math.h, stdlib.h etc)
 



Variables in C:
 * They must be decleard before use.
 * types include int, float and many more.
 * Uninitialized variables in C get a default value;
 * Variables can be initialized on or after creation. 
   i.e. 
     * Initialized on creation:
       int n = 3; (variable created and initialized)

     * Initialized after creation:
       int n; (variable created)
       n = 3; (variable initialized)

   Arithmetic Operations: Very similar to other newer languages:
     * 'variable 'operator 'variable

   Semicolons end statements (it's actually very necessary here).  

   Order of operations can be overwritten using parentheses (like newer languages).


Functions in C:
  * function prototypes:
    int factorial (int); or
    int factorial (int n);

  * General form of functions in C.
     *return_type function_name(arg1, arg2,...);*
       * args:        arguments passed to the funciton
       * return_type: single value returned to caller of function. (can be void; meaning no return value/arguments) 




The main() function:
  main() is the entry point to a C prograam
Example 1:
```
int main(void) {
  puts("Hello there");

  return 0;
}
```

Example 2 (storing message inside a variable):
```
int main(void) {
  const char msg[] = "Hello there";

  puts(msg);

  return 0;
}
```
  const -> qualifies variable as a constant 
  char  -> datatype in C representing a single character
  const char msg[] -> a constant array of characters.


Strings:
  * strings in C are stored as character arrays.
  * they are null terminated (i.e. last character in a string array is '\0' null)
  * special characters can be added in strings using \ (escape) eg: \b (backspace) \\ (backslash) \t (tab) etc.


Some I/O:
* puts(string)   -> prints string to stdout
* putschar(char) -> prints character to stdout
* char = getChar() -> return character from stdin etc.


Preprocessor Macros:
  preprocessor macros begin with the # character
  examples:
   #include <stdio.h>   -> makes stdio available in file
   #define msg "hello"; -> defines msg as "hello" throughout file 

  marcos can also be expressions
  example:
  #define add3(x,y,z) ((x)+(y)+(z))
  define can take arguments and be treated like a function, although it is not suitable for recursive functions (due compliers peforming inline replacement).

  conditional preprocessor macros:
   * #if, #ifdef, #ifndef, #else, #elif, #endif, etc.
     Conditional macros can control which lines are even complied; they are evaluated before the code itself is complied.
     Due to conditional macros begin evaluated before code is complied, conditions must also be preprocessors defines or literals.
     checkout: #pragma #error #warning #undef

Steps to running C code
* Compile (with gcc for example)
* gdb filename.0
* ./filename


 

