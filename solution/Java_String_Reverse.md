# Day #20 - Java Sting Reverse
## Problem


A palindrome is a word, phrase, number, or other sequence of characters which reads the same backward or forward.

Given a string `A`, print Yes if it is a palindrome, print No otherwise.

***Constraints***

+ `A` will consist at most `50` lower case english letters.
***Sample Input***
```

madam

```
***Sample Output***
```

Yes

```

## Solution
```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        
        Scanner sc=new Scanner(System.in);
        String A = sc.next();
        String reverse = "";
        int length = A.length();
        for (int i=length-1;i>=0;i--){
            reverse = reverse + A.charAt(i);
        }
        boolean ans = A.equals(reverse);
        if (ans) {
            System.out.println("Yes");
        } else {
            System.out.println("No");
        }        
    }
}

```
