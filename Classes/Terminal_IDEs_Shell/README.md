# Terminal, Shell, and IDE Shell Usage

## Definintions
### Shell 
A program that provides a command-line interface, letting users interact with the operating system by typing commands such as navigating folders, running programs, or managing files.

### Terminal
A text-based interface that allows the user to write commands to the shell. Most computers will have a default terminal, but different programs may have their own terminals that can converse with the computer's operating system as well. Note that different operating systems may use different languages. 

### Shell Scripting
The practice of writing those commands in a text file (a script) so they can be executed automatically in sequence, allowing users to automate tasks, manage workflows, and save time on repetitive operations. These files will typically come as a batch or .bat file on Windows and a shell or .sh file on macOS. 

### IDE
An integrated development environment is a software application that provides comprehensive facilities for software development. An IDE normally consists of at least a source-code editor, build automation tools, and a debugger. Examples of an IDE are VSCode, RStudio, PyCharm, and NetBeans.

## Using the Terminal
### Benefits of Terminal Use
- * Allows for faster access to all available commands
- * Enables users to work directly with any part of the system (files, processes, memory locations, etc.)
- * No mouse is neccessary when using terminal
- * Error messages given directly

## Finding Your Terminal
The Terminal will vary for different operating systems: 

**For Mac:** In your computer's search, type "Terminal". Click the app to open.

**For Windows:** From the Start menu, type "Command Prompt". Click the app to open.

## Terminal Usage
Now that the app is open, it will usually appear as a small, mostly-blank window with a line of text in the top left. You will always work in the line farthest to the bottom. The line at the bottom will provide some information about where you're working, including where in the directory you're working. 

Some Terminals are particular about how you write in it. For example, you may not be able to "go back" with your cursor to correct a typo; instead, you may have to backspace back to the point in the mistake.

## Some terminal/command line basics:
- * pwd = print working directory; sending this command will ask the computer to return an answer to the question "where am I working right now?"
- * ls = list; sending this command will ask the computer the question "what are the other items in the folder where I'm working?"
- * cd [folder] = change directory; goes into a folder in the directory you're in. inside the [brackets] you'll put the name of the folder you want to work in.
- * cd .. = change directory, go up one level

- * and many more! feel free to google other commands specific for your operating system

### Using an Internal Shell
Most IDEs have an built-in terminal which allows the user to interact with their computer environment without leaving the IDE. This allows the user to run external commands and perform build tasks which helps with long chain workflows. This level of integration requires the IDE to be present in the systems' PATH envrionment. 