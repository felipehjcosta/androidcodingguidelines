# Android Coding Guidelines
================

This document contains the coding guidelines for the Android Development. It contains four major sections:

- Style Guidelines, on how to organize your source code.
- Git Workflow Changes, discusses how Git workflow works.
- Source Code Control, details our source code control use.
- Best Practices, used in the Android Development.

## Style Guidelines

In order to keep the code consistent, please use the following conventions. From here on `good' and `bad' are used to attribute things that would make the coding style match, or not match. It is not a judgment call on your coding abilities, but more of a style and look call. Please try to follow these guidelines to ensure prettiness.

You may also wish to read the [Code Conventions for the Java Programming Language](http://www.oracle.com/technetwork/java/codeconv-138413.html) as well, however the Android guidelines below take precedent for Java code if there is a conflict.

# Naming Conventions

1. Use Meaningful Names

Choose names that suggest their purpose. Good names help you understand the problem you are solving.

Good:
	int count;
    
Bad:
	int i;


2. Variable Names

Start with a lower-case letter and use uppercase letters as separators. Do not use under bars ('_').

int myVar
3. Constant Names

Use all capital letters and use under bars ('_') as separators.

final int MY_CONST = 1;
4. Method Names

Start with a lower-case letter and use uppercase letters as separators. Do not use under bars ('_').

int myMethod()
5. Class Names

Start with an upper-case letter and use uppercase letters as separators. Do not use under bars ('_').

public class MyClassName

