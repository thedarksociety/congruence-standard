Congruence, for Bash
====================

A _____ of bash for ______ .

Table of Contents
-----------------

1. [Introduction]()

2. Organization

Code Style

##### Shebang

Google suggests the `#!/bin/bash` syntax; however, not all Unix and Unix-like
operating systems have bash installed. That said, use `#!/usr/bin/env bash`.

I use 2-space tabs.

I always quote variables unsure of (mixed, characters).

less quotes, but quote.

### Introduction

### Parameter Expansions

#### Basics

The [[]] is safer and should always be used.

#### Substitution
#### length
#### Default
#### Comments

Each file must begin with a description of its contents.

Each file MUST have a top-level comment including a brief overview if its
contents. A copyright, author, and other information is optional.

```shell
# !/usr/env/bin bash
#
# This is a brief description of the script on the heading.
```

#### SUbstrings
#### Manipulation


### Loops

#### Basics
#### Reading Lines
#### Ranges
#### Forever
#### Examples

### Functions

#### Defining
#### Returning Values
#### Arguments
#### Raising Errors

### Conditionals

#### Conditoins
#### examples

### Arrays

#### Defining Arrays
#### Working with Arrays
#### Operations
#### Iteration


### Dictionaries
#### Defining Dictionaries
#### Working with
#### Interation

### Options
#### options
#### glob options

#### history
#### Commands
#### Operations
#### Expansions
#### Slices

### Misc

#### numbers and calculations
#### inspecting caommands
#### trap errors
#### source relative
#### transforming Strings
#### subshells
#### redirection
#### case/switch
#### printf
#### directories
#### getting Options
#### heredoc
#### special vars
#### command results
#### reading input
#### checks




1. general styles
  length
  indenting
2. commenting
  intro comments
  line ending comments
  section comments
  function comments
  commenting style
3. variables and constants
  use of Variables
  use of constants
4. Success verification
  command line Options
  vars, caommands, functions
  execution and summary
5. files
6. command line options
7. built in shell Commands
8. portability
9. SUID/SGID
10. testing
  syntax checks
  test scope
  use of echo
  use of bash options
  use of PS4
  use of trap
  use of bashdb
11. more resources
12. summary
