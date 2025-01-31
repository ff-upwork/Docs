{
  "date" : "2021-07-23",
  "keywords" : [ "PL", "file", "extension", "format", "Perl", "Perl language", "PL files", "programming"],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about PL file format and APIs that can create and open PL files.",
  "title" : "PL File - Perl Script File Format",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-07-23"
}

## What is a PL file?

A file with .pl extension is a Perl Script file that is a scripting language. These are compiled and run using Perl Interpreter software. A PL script file contains lines of code, variables, and comments. Scripting languages are comparatively difficult to
understand to other programming file formats such as [PHP](/programming/php/). PL files can be created and are compatible with Windows, macOS, and Linux.

## Brief History of Perl Scripting Language

This language was first kept in use in 1987, so these files got their origin in that year. In 1989 the Perl 2 was released. Later on, it has been updated and has been modified up to the 5.35 version, and the next version is targeted to be released next year.

In every update, there have been added tools about the functionality, performance, and look of the language and files. There have been many revisions about the versions in these years. It was originally a basic scripting language but now it comprises many other modules too. Originally, it was a very simple language, but the scripts of this language were quite difficult to understand as they were compact.

## Perl File Format Extension Specifications

There are some properties or specifications of these programming files, some of them are as follows:

*	The code included in these files is in plain text format and used for script development
*	Scripting of server, parsing of text, and server administration are the main aspects that the script of this language covers
*	Many popular programs that are associated with this language are Active state Active Perl and Bare Bones BBEdit (compatible with Mac OS)
*	This language is considered a high-level language
*	For Win32, the user may have to install native binary distribution of the language
*	It requires some scripting tools to become executable in various Windows Resource Kits
*	Visual Studio .NET is a famous framework for the development of programming languages. The Active State tool known as Visual Perl is used to add Perl into Visual studio
*	In the files, the first line of the source code describes the information of the interpreter being used. The PL files usually start with **#!/usr/bin/perl** line that tells your computer to run this script using a Perl interpreter installed in the computer


## PL Script Examples

```
#!/usr/bin/perl
print "Hello, world\n";
```

This will print

```
Hello, World
```

### Single line comment ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Multi line comment ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Variable assignment ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Scalar variable assignment ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Simple scalar operations ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## References ##

- [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))
