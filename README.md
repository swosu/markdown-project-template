# Project Name

## Introduction 
This is where my project introduction would go.  This would include information about what the source code does and its purpose.  This paragraph would also include methods used such as Math.*random()* or even custom methods.

## Project Outline
1.   Item 1
    *   Sub-Item a
    *   Sub-Item b
2.   Item 2
3.   Item 3
4.   Item ...

The Project Outline can also be represented in this format:
```java
//Declaring variables
//Doing other things
//Other line comments used in outlining
```


##  References & Literature
*   Reference 1 URL: [Link Example](http://example.net/)
   *   Write 2-3 sentences about your source and why you chose it.
*   Reference 2 Book: MLA
    *   Liang, Y. Daniel. *Introduction to Java Programming: Comprehensive Version.* 10th ed. N.p.: Pearson, 2014. Print. 
*   Reference 3 Book: APA
    *   Liang, Y. (2014). *Introduction to Java programming: Comprehensive version* (Tenth ed.). 

## Source Code
```java
import java.io.File;
import java.util.Scanner; 

public class CheckPalindrone {
  public static void main(String[] args) {
    // Prompt the user to enter a directory or a file
    System.out.print("Enter a directory or a file: ");    
    Scanner input = new Scanner(System.in);
    String directory = input.nextLine();
    
    // Display the size
    System.out.println(getSize(new File(directory)) + " bytes");
  }

  public static long getSize(File file) {
    long size = 0; // Store the total size of all files

    if (file.isDirectory()) {
      File[] files = file.listFiles(); // All files and subdirectories
      for (int i = 0; files != null && i < files.length; i++) {
        size += getSize(files[i]); // Recursive call
      }
    }
    else { // Base case
      size += file.length();
    }

    return size;
  }
}
```

## Console Output
```
Enter a string: banana
a appears  3 times
b appears  1 time
n appears  2 times
```

## Command Prompt Output
```
Microsoft Windows [Version 6.1.7601]
Copyright (c) 2009 Microsoft Corporation.  All rights reserved.

C:\Users\LAB>cd desktop

C:\Users\LAB\Desktop>mkdir test

C:\Users\LAB\Desktop>cd test

C:\Users\LAB\Desktop\test>git init
Initialized empty Git repository in C:/Users/LAB/Desktop/test/.git/

C:\Users\LAB\Desktop\test>echo hello >> Readme.md

C:\Users\LAB\Desktop\test>git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        Readme.md

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\LAB\Desktop\test>git add .

C:\Users\LAB\Desktop\test>git commit -m "initial commit"
```

## Summary
For this assignment ... etc so on and so forth
