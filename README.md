# ALX Simple Shell Team Project
This is ALX simple shell project. This was done collaboratively. We where asked to create a simple shell that mimics the Bash shell used on Ubuntu and Linux systems. hsh will be used to prompt our shell.

# Project was developped using the following code / language

    1. C language - Main coding language for the project
    2. Shell - Vi waas used 
    3. Betty linter - used to check the file for currect syntax. 

# General Requirement for project

    1. Allowed editors: vi, vim, emacs
    2. All your files will be compiled on Ubuntu 20.04 LTS using gcc, using           the options -Wall -Werror -Wextra -pedantic -std=gnu89
    3. All your files should end with a new line
    4. A README.md file, at the root of the folder of the project is                mandatory
    5. Your code should use the Betty style. It will be checked using betty-         style.pl and betty-doc.pl
    6. Your shell should not have any memory leaks
    7. No more than 5 functions per file
    8. All your header files should be include guarded
    9. Use system calls only when you need to (why?)
    10. Write a README with the description of your project
    11. You should have an AUTHORS file at the root of your repository,               listing all individuals having contributed content to the repository.         Format, see Docker

# Main Learning Objectives

  1. Who designed and implemented the original Unix operating system
  2. Who wrote the first version of the UNIX shell
  3. Who invented the B programming language (the direct predecessor to the        C programming language)
  4. Who is Ken Thompson
  5. How does a shell work
  6. What is a pid and a ppid
  7. How to manipulate the environment of the current process
  8. What is the difference between a function and a system call
  9. How to create processes
  10. What are the three prototypes of main
  11. How does the shell use the PATH to find the programs
  12. How to execute another program with the execve system call
  13. How to suspend the execution of a process until one of its children           terminates
  14. What is EOF / “end-of-file”?

# Description

    hsh is a simple UNIX interpreter that gets command from a file or from a       user input and executes them 

# How hsh works
      1. Prints a prompt and waits for a command from the user
      2. Creates a child process in which the command is checked
      3. Checks for built-ins, aliases in the PATH, and local executable              programs
      4. The child process is replaced by the command, which accepts                   arguments
      5. When the command is done, the program returns to the parent process           and prints the prompt
      6. The program is ready to receive a new command
      7. To exit: press Ctrl-D or enter "exit" (with or without a status)
      8. Works also in non interactive mode
      
# Compilation
      gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o dash
      

# List of allowed functions and system calls
    1. access (man 2 access)

      access, faccessat, faccessat2 - check user's permissions for a
      file. It checks if the user has a read/write and execute permission. 

    2. chdir (man 2 chdir)

       fchdir - Used to change working directory!

    3. close (man 2 close)

          chdir() changes the current working directory of the calling
           process to the directory specified in path.
       fchdir() is identical to chdir(); the only difference is that the
           directory is given as an open file descriptor.

    4. closedir (man 3 closedir)

        close() closes a file descriptor, so that it no longer refers to
           any file and may be reused.  Any record locks (see fcntl(2)) held
           on the file it was associated with, and owned by the process, are
           removed (regardless of the file descriptor that was used to
           obtain the lock)

    5. execve (man 2 execve)
    6. exit (man 3 exit)
    7. _exit (man 2 _exit)
    8. fflush (man 3 fflush)
    9. fork (man 2 fork)
    10. free (man 3 free)
    11. getcwd (man 3 getcwd)
    12. getline (man 3 getline)
    13. getpid (man 2 getpid)
    14. isatty (man 3 isatty)
    15. kill (man 2 kill)
    16. malloc (man 3 malloc)
    17. open (man 2 open)
    18. opendir (man 3 opendir)
    19. perror (man 3 perror)
    20. read (man 2 read)
    21. readdir (man 3 readdir)
    22. signal (man 2 signal)
    23. stat (__xstat) (man 2 stat)
    24. lstat (__lxstat) (man 2 lstat)
    25. fstat (__fxstat) (man 2 fstat)
    26. strtok (man 3 strtok)
    27. wait (man 2 wait)
    28. waitpid (man 2 waitpid)
    29. wait3 (man 2 wait3)
    30. wait4 (man 2 wait4)
    31. write (man 2 write)
