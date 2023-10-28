# Day #19 - Java String Comparision
# Problem

We define the following terms:

+ Lexicographical Order, also known as alphabetic or dictionary order, orders characters as follows:<br>
 ``` A < B < . . .  < Y < Z < a < b < . . . < y < z```<br>
For example, ball < cat, dog < dorm, Happy < happy, Zoo < ball.

+ A substring of a string is a contiguous block of characters in the string. For example, the substrings of abc are a, b, c, ab, bc, and abc.
Given a string, `s`, and an integer, `k`, complete the function so that it finds the lexicographically smallest and largest substrings of length `k`.

***Function Description***

Complete the getSmallestAndLargest function in the editor below.

getSmallestAndLargest has the following parameters:

+ string s: a string
+ int k: the length of the substrings to find
  
***Returns***

+ string: the string ' + "\n" + ' where and are the two substrings
  
***Input Format***

The first line contains a string denoting `s`.
The second line contains an integer denoting `k`.

***Constraints***

+ 1 ≤ |s| ≤ 100
+ '`' consists of English alphabetic letters only (i.e., [a-zA-Z]).
  
***Sample Input***
```

welcometojava
3

```
***Sample Output***
```

ava
wel

```
***Explanation***

String `s = "welcometojava"` has the following lexicographically-ordered substrings of length `k = 3`:
["ava", "com", "elc", "eto", "jav", "lco", "met", "oja", "ome", "toj", "wel"]

We then return the first (lexicographically smallest) substring and the last (lexicographically largest) substring as two newline-separated values (i.e., ava\nwel).

The stub code in the editor then prints ava as our first line of output and wel as our second line of output.

## Solution
```java
import java.util.Scanner;

public class Solution {

    public static String getSmallestAndLargest(String s, int k) {
      String currStr = s.substring(0, k);
      String smallest = currStr;
      String largest = currStr;
      
      for (int i = k; i < s.length(); i++) {
            currStr = currStr.substring(1, k) + s.charAt(i);
            if (largest.compareTo(currStr) < 0)     
                 largest = currStr;
            if (smallest.compareTo(currStr) > 0)
                 smallest = currStr;            
        }  
        
      return smallest + "\n" + largest;
    }


    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String s = scan.next();
        int k = scan.nextInt();
        scan.close();
      
        System.out.println(getSmallestAndLargest(s, k));
    }
}
```
