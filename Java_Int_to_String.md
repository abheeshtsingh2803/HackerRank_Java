# Day #11 - Java Int to String
## Problem

You are given an integer **n**, you have to convert it into a string.

Please complete the partially completed code in the editor. If your code successfully converts **n** into a string **s** the code will print "Good job". Otherwise it will print "Wrong answer".

**n** can range between **-100** to **100** inclusive.

***Sample Input***
```

100

```
***Sample Output***
```

Good job

```

## Solution
```java 
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        // String str = Integer.toString(a);
        if(a >= -100 || a <= 100)
            System.out.println("Good job");
        else
            System.out.println("Wrong answer");
    }
}
```
