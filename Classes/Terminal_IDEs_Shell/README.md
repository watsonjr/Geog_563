# Terminal, Shell, and IDE Shell Usage

## Definintions
### Shell 
A program that provides a command-line interface, letting users interact with the operating system by typing commands such as navigating folders, running programs, or managing files.

### Terminal
A text-based interface that allows the user to write commands to the shell. Most computers will have a default terminal, but different programs may have their own terminals that can converse with the computer's operating system as well. Note that different operating systems may use different languages. 

Some terminal/command line basics:
- * pwd = print working directory; answers the question "where am I working right now?"
- * ls = list; answers the question "what are the other items in the folder where I'm working?"
- * cd [folder] = change directory; goes into a folder in the directory you're in. inside the [brackets] you'll put the name of the folder you want to work in.
- * cd .. = change directory, go up one level

### Shell Scripting
The practice of writing those commands in a text file (a script) so they can be executed automatically in sequence, allowing users to automate tasks, manage workflows, and save time on repetitive operations. These files will typically come as a batch or .bat file on Windows and a shell or .sh file on macOS. 

### IDE
An integrated development environment is a software application that provides comprehensive facilities for software development. An IDE normally consists of at least a source-code editor, build automation tools, and a debugger. Examples of an IDE are VSCode, RStudio, PyCharm, and NetBeans.

## Using an Internal Shell
Most IDEs have an built-in terminal which allows the user to interact with their computer environment without leaving the IDE. This allows the user to run external commands and perform build tasks which helps with long chain workflows. This level of integration requires the IDE to be present in the systems' PATH envrionment. 