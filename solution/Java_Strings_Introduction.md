# Day #17 - Java Strings Introduction
## Problem

This exercise is to test your understanding of Java Strings. A sample String declaration:
```

String myString = "Hello World!"

```
The elements of a String are called characters. The number of characters in a String is called the length, and it can be retrieved with the String.length() method.

Given two strings of lowercase English letters, **A** and **B**, perform the following operations:

1. Sum the lengths of **A** and **B**.
2. Determine if **A** is lexicographically larger than **B** (i.e.: does  come before  in the dictionary?).
3. Capitalize the first letter in **A** and **B** and print them on a single line, separated by a space.

***Input Format***

The first line contains a string **A**. The second line contains another string **B**. The strings are comprised of only lowercase English letters.

***Output Format***

There are three lines of output:
For the first line, sum the lengths of **A** and **B**.
For the second line, write Yes if **A** is lexicographically greater than **B** otherwise print No instead.
For the third line, capitalize the first letter in both **A** and **B** and print them on a single line, separated by a space.

***Sample Input***
```

hello
java

```
***Sample Output
```

9
No
Hello Java

```
***Explanation***

String **A** is "hello" and **B** is "java".

**A** has a length of **5**, and **B** has a length of **4**; the sum of their lengths is **9**.
When sorted alphabetically/lexicographically, "hello" precedes "java"; therefore, **A** is not greater than **B** and the answer is No.

When you capitalize the first letter of both **A** and **B** and then print them separated by a space, you get "Hello Java".

## Solution
```java

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        
        Scanner sc=new Scanner(System.in);
        String A=sc.next();
        String B=sc.next();
        /* Enter your code here. Print output to STDOUT. */
                  
      System.out.println(A.length()+B.length());
        int i = A.compareTo(B);
        if(i>0){
             System.out.println("Yes");
        } else{
             System.out.println("No");
        }
        String atemp = A.substring(0,1).toUpperCase()+A.substring(1);
        String btemp = B.substring(0,1).toUpperCase()+B.substring(1);;
        System.out.println(atemp+" "+btemp); 
    }
}

```
