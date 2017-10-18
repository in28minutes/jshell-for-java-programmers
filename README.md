# JShell for Java Programmers
An introduction to JShell for Java Programmers

## Notes

- Clear Screen

```
System.out.print("\033[H\033[2J");
```

## Course Details

### Introduction to JShell
- Java REPL (Read Evaluate Print Loop) Shell
- Comes by default with JDK 9
- Quickly debug or test or investigate an API or try a new Library
- Quick Learning with immediate feedback. No need to write a PSVM or a Unit test.

### Launching JShell
- Install JDK 9
- Open Command Prompt and type in jshell
- Other option is to cd to the bin folder where JDK 9 is installed and type in jshell
- /exit
- Quick Tip - Nothing is saved by default!
- Quick Tip - Verbose mode! jshell -v

### JShell Basics - Variables and Expressions
- int i=10;
- int i=10; int j=10; //multiple statements
- System.out.println(i);
- i = i + j
- Tip : Semicolon is not mandatory unless you want to seperate statements on a single line.
- Tip : Comments are supported //


### JShell Basics - Multiple Lines
- i = 
    -   i + j
- Multi line comments


### JShell Tip : Implicit Variables
- When expression returns a value
- 10 + 10
- System.out.println($1)

### JShell Tip : Feedback options
- /set feedback verbose
- silent | normal | concise

### JShell Tip : Access modifiers are Ignored Outside a class
- public, protected and private are ignored outside a class
- final and static are also ignore

### JShell Basics - Methods

```
int cube(int n) {
    return n * n * n; 
}

void printTwice(String str) {
	System.out.println(str);
	System.out.println(str);
}
```

### JShell Basics - Imports
- Default imports
- /imports
- importing a new class 
  - 2 options - import statement or auto import
  - import java.sql.Timestamp
  - new Timestamp => Shift + Tab i
- Creating a new variable using imported class  
  - new Timestamp(); => Shift + Tab v
  - new Timestamp(1000L);=> Shift + Tab v
  - Timestamp temp = new Timestamp(1000L);

### JShell Tip : Forward Referencing
- methods
- constants
- variables
- Cannot be used in variable initialization

### JShell Basics - Class
- Basic Class
- Editing a class using external editor
- /edit
- /edit Course
- Course course1 = new Course()
- course1.setName("Microservices with Spring Boot");
- Cannot access private variables in a class - course1.name 

### JShell Tip - Auto completion
- Class in a package
- Class members
- Parameters
- Overloaded methods
- Documentation of a Class

### JShell Commands - Help
- All commands start with / - slash or forward slash
- /help, /?, / followed by tab

### JShell Commands - list, drop and history
 - numerical identifier
 - /drop
 - /history

### JShell Commands - var, methods and types

### JShell Tip : Exceptions and Line Numbers

### Saving and Reloading JShell Sessions
- /save file.jsh
- /open file.jsh

### JShell Tip - Open Existing Java File


### JShell - Setting Custom Start Options
- Getting a command to be executed at start of JShell
```
/reset
System.out.print("\033[H\033[2J");
/list
/save start.jsh
/set start start.jsh
/reset
/list
/list -all
/set start start.jsh DEFAULT
/reset
/list
/list -all
/history
```
- JShell Tip - For the Lazy Guys
```
/set start -retain DEFAULT PRINTING
```
### JShell Tip - More Save and List Options - history, all and start

### JShell - Playing around with an External Library
- /env -class-path commons-lang3-3.6.jar
- StringUtils.trim("1234 ");

### JShell Tip - Shortcuts to commands and options
- /l
- /h
- /l -a

### JShell Tip - Navigation
- Ctrl + a
- Ctrl + e
- Ctrl + k

### Jshell Tip - Search Snippets
- Ctrl + r
- Ctrl + s

### Thank You


## Code Examples from Course

