# Holberton-Monty Repository
>Monty: A Custom Monty Bytecode Interpreter
<p align="center">
  <img src="https://i.ibb.co/qCHmRsb/Monty-Python-title.jpg">
</p>

## Learning Objectives

* What do LIFO and FIFO mean
* What is a stack, and when to use it
* What is a queue, and when to use it
* What are the common implementations of stacks and queues
* What are the most common use cases of stacks and queues
* What is the proper way to use global variables

## Compilation & Output

* Code will be compiled this way:
```C
$ gcc -Wall -Werror -Wextra -pedantic *.c -o monty
```
* Any output will be printed on stdout
* Any error message will be printed on stderr

## The Monty Language

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It
relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create
an interpreter for Monty ByteCodes files.

Files containing Monty byte codes usually have the .m extension. Most of the industry uses this
standard but it is not required by the specification of the language. There is not more than one
instruction per line. There can be any number of spaces before or after the opcode and its argument.

Monty byte code files can contain blank lines (empty or made of spaces only), and any additional text
after the opcode or its required argument is not taken into account.

## The Monty Program

* Usage: `monty file`
    * where `file` is the path to the file containing Monty byte code
* If the user does not give any file or more than one argument to the program, it will print the error message `USAGE: monty file` and exit with the status `EXIT_FAILURE`
* If, for any reason, it’s not possible to open the file, it will print the error message `Error: Can't open file <file>` and exit with the status `EXIT_FAILURE`
    * where `<file>` is the name of the file
* If the file contains an invalid instruction, it will print the error message `L<line_number>: unknown instruction <opcode>` and exit with the status `EXIT_FAILURE`
    * where `<line_number>` is the line number where the instruction appears and `<opcode>` is the instruction given
    * line numbers always start at 1
* The monty program runs the bytecodes line by line and stop if either:
    * it executed properly every line of the file
    * it finds an error in the file
    * an error occured
* If the program can't malloc anymore, it will print the error message `Error: malloc failed`, followed by a new line, and exit with status `EXIT_FAILURE`.

## Other

* The folder **bytecodes** contains different monty byte code files that serve
for testing purposes.

* *gcc_monty* is a script that will compile the program with the above mentioned
specifications.

* *leaks_check* is a script to be used with the monty byte code file to check
for any memory leaks after the execution of the program.

## Built With

  - [Ubuntu](https://ubuntu.com/) 
  - [GitHub](https://github.com/)
  - [PurpleBooth](https://github.com/PurpleBooth)

## Authors

  - **Raul** - [*@RaulAcosta*](https://github.com/RaulAcosta)
  - **Angeira** -[*@AngeiraT*](https://github.com/AngeiraT)

## License

This project is licensed under the Holberton School Software Engineering Program.

## Acknowledgments

  - Approaching a Project
  - Group Projects
  - Cohort 18
  - How do I use extern to share variables between source files in C?

## References
  - [Monty Language](https://en.wikipedia.org/wiki/Unix_shell)
  - [Monty Programs](https://en.wikipedia.org/wiki/Ken_Thompson)
