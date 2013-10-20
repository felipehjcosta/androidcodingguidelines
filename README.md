# Android Coding Guidelines

This document contains the coding guidelines for the Android Development. It contains four major sections:

- Style Guidelines, on how to organize your source code.
- Git Workflow Changes, discusses how Git workflow works.
- Source Code Control, details our source code control use.
- Best Practices, used in the Android Development.

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
	public class MyclassName_
```


#### Curly Braces

A fervent issue of great debate in programming circles is placement of curly braces. The Java style is to place the initial brace on the same line as the keyword and the trailing brace on its own line but lined up with the keyword. For example:

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


#### Whitespace

Always layout your source code so that elements that are part of a group go together.

##### No Tab Character

Do not have any tab characters in your source code. It is difficult to impossible to read source code if your tab settings are different than the authors.

The easy way to remove tabs is to set your text editor to substitute the correct number of spaces for a tab character. See the instructions for both jEdit and TextPad for setting up these editors. For other editors, you will need to search for the setting.

##### Line Length

Limit your line length to 80 characters since longer lines may cause problems with many text editors and other tools.

##### Spacing Around Operators

Always put spaces before and after binary operators. This improves the readability of expressions. For example:

```
int c = -a * b - d;
```

##### Indentation

Always indent within curly braces. Use four (4) spaces for each indentation level. For example:
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

Always line up if statements with the curly braces for their associated else statement. Specifically, place the initial brace on the same line as the keyword and the trailing brace inline on the same line as the next statement. For example:

```
if (condition) {               // Comment
    ...
} else if (condition) {        // Comment
    ...
} else {                       // Comment
    ...
}
```














