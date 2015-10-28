# Project Name
This is where my project description would go

## Code

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

C:\Users\LAB\Desktop\test>echo hello >> readme.md

C:\Users\LAB\Desktop\test>git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        readme.md

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\LAB\Desktop\test>git add .

C:\Users\LAB\Desktop\test>git commit -m "initial commit"
```

## Summary
For this assignment ... etc so on and so forth
