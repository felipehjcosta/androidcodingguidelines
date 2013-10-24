# Android Coding Guidelines

This document contains the coding guidelines for the Android Development. It contains four major sections:

- Style Guidelines.
- Git Workflow Changes.
- Source Code Control.
- Best Practices.

## Style Guidelines

In order to keep the code consistent, please use the following conventions. From here on `good' and `bad' are used to attribute things that would make the coding style match, or not match. It is not a judgment call on your coding abilities, but more of a style and look call. Please try to follow these guidelines to ensure prettiness.

You may also wish to read the [Code Conventions for the Java Programming Language](http://www.oracle.com/technetwork/java/codeconv-138413.html) as well, however the Android guidelines below take precedent for Java code if there is a conflict.

### Naming Conventions

#### Use Meaningful Names

Choose names that suggest their purpose. Good names help you understand the problem you are solving.

**Good:**
```
int count;
```
    
**Bad:**
```
int i;
```

#### Variable Names

Start with a lower-case letter and use uppercase letters as separators. Do not use under bars ('_').

**Good:**
```
int myVar;
```

**Bad:**
```
int my_var;
```

#### Constant Names

Use all capital letters and use under bars ('_') as separators.

**Good:**
```
final int MY_CONST = 1;
```
    
**Bad:**
```
final int myConst = 1;
```

#### Method Names

Start with a lower-case letter and use uppercase letters as separators. Do not use under bars ('_').

**Good:**
```
int myMethod();
```

**Bad:**
```
int My_Method();
```

#### Class Names

Start with an upper-case letter and use uppercase letters as separators. Do not use under bars ('_').

**Good:**
```
	public class MyClassName
```

**Bad:**
```
	public class My_class_Name
```


### Curly Braces

The Java style is to place the initial brace on the same line as the keyword and the trailing brace on its own line but lined up with the keyword.

**Good:**
```
if (condition) {
    ...
}

while (condition) {
    ...
}
```

**Bad:**
```
if (condition) 
{
    ...
}

while (condition) 
{
    ...
}
```

#### When Braces are Needed

All if, while and do statements must either have braces or be on a single line. This helps to make sure someone adding a line of code does not forget to add braces.

### Whitespace

Always layout your source code so that elements that are part of a group go together.

##### No Tab Character

Do not have any tab characters in your source code. It is difficult to impossible to read source code if your tab settings are different than the authors.

The easy way to remove tabs is to set your text editor to substitute the correct number of spaces for a tab character. See the instructions for both jEdit and TextPad for setting up these editors. For other editors, you will need to search for the setting.

##### Line Length

Limit your line length to 80 characters since longer lines may cause problems with many text editors and other tools.

##### Spacing Around Operators

Always put spaces before and after binary operators. This improves the readability of expressions.

```
int c = -a * b - d;
```

##### Indentation

Always indent within curly braces. Use four (4) spaces for each indentation level. 

```
void func() {
    if (something happened) {
        if (another thing happened) {
            while (more input) {
                ...
            }
        }
    }
}
```

##### if-else-if-else

Always line up if statements with the curly braces for their associated else statement. Specifically, place the initial brace on the same line as the keyword and the trailing brace inline on the same line as the next statement.

```
if (condition) {               // Comment
    ...
} else if (condition) {        // Comment
    ...
} else {                       // Comment
    ...
}
```

### Additions and Exceptions to the Javadoc Standards

Most professional Java programmers follow these conventions even though they are not listed in the Code Conventions for the Java Programming Language.

##### No Magic Numbers

A magic number is a numeric literal that is not defined as a constant. It's magic because no one has a clue what it means after 3 months, including the author. From widespread use, -1, 0, 1, and 2 are not considered magic numbers.

Whenever you assign a number to a variable, use a constant instead. In Java, you declare constants, which are variables that cannot change, using the keyword final. You may use local constants within methods or member constants declared outside of any method. Usually, you declare member constants as a public static final member variable.

```
public static final int MY_CONSTANT = 10;
```

Because of their special meaning, write constants in all upper case and use under bars ('_') as separators.

##### Method Length

Methods must be no more than 150 lines long. If a method becomes very long it is hard to understand. Instead, you should create smaller methods that focus on individual tasks. This is good for TEST!

##### Tab Character

Do not have any tab characters in your source code. It is difficult to impossible to read source code if your tab settings are different than the authors.


### Comments

Comments are explanatory notes for the humans reading a program. With good name choices, comments can be minimal in a program. The only required comments are block comments just before the class declaration (after any import statements) and just before each method declaration.

Other than block comments, one other time to add comments is when your code is unusual or obscure. When something is important and not obvious, it merits a comment.

#### Block Comments

Javadoc is a program that examines the declarations and documentation comments of your code to produce a set of HTML pages. These pages describe your code to other programmers. For an example of the documentation produced, see the Java API documentation.

Some of the Javadoc is derived from specially-formatted block comments, which you create as follows:

- Indent the first line to align with the code below the comment.
- Start the comment with the begin-comment symbol (/**) followed by a return.
- Start subsequent lines with an asterisk *. Indent the asterisks with an additional space so the asterisks line up. Separate the asterisk from the descriptive text or tag that follows it.
- Add a description of the purpose of the class or method.
- Insert a blank comment line between the description and the list of tags, as shown.
- Insert additional blank lines to create various tags.
- The last line begins with the end-comment symbol (*/) indented so the asterisks line up and followed by a return. Note that the end-comment symbol contains only a single asterisk.

```
/**
 * The main method for the HelloWorld program.
 *
 * @param args Not used
 */
 ```
 
#### File Comment Block

Every source code file (*.java) must have a Javadoc comment block just before the class declaration containing the course number, assignment number, name of the file and purpose of the file. One or two lines is usually sufficient to explain the purpose. In addition, you must add the author tag containing your name and the version tag containing the date the assignment is due. For example:

```
import javax.swing.*;

/**
 * CS-12J Asn 3
 * HelloWorld.java
 * Purpose: Prints a message to the screen.
 *
 * @author Jane User
 * @version 1.0 8/20/03
 */
public class HellowWorld {
```

The following tags must be used always:

@author
@version

#### Method Comment Block

Every method must have a Javadoc comment block before the method. For example:

```
/**
 * Read a line of text from the shell console.
 *
 * @return A String input by the user.
 */
The first line is a description of how to use the method.
```

Where appropriate, the following tags must be used:

@param
@return
@throws







