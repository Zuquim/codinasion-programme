---
title: Check palindrome number
description: Write a program to check palindrome number
tags:
  - python
  - java
  - cpp
  - c
contributors:
  - NeelPatel31
  - seraph776
---

## Write a program to check palindrome number.

```txt
Input  : 121
Output : Palindrome number
```

---

<CodeBlock>

```python
def check_palindrome(n: int) -> str:
    """Checks if n is a palindrome"""
    if str(n) == str(n)[::-1]:
        return 'Palindrome Number'
    return 'Not Palindrome Number'


num = int(input('Input  : '))
print('\nOutput :', check_palindrome(num))
```

```java
import java.util.*;

public class solution {
    public static String checkPalindrome(int a) {
        int pal = 0, n;
        int original = a;
        while (a > 0) {
            n = a % 10;
            pal = pal * 10 + n;
            a = a / 10;
        }
        if (original == pal) {
            return "Palindrome number";
        }
        return "Not palindrome number";
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Input  : ");
        int num = sc.nextInt();
        System.out.println("Output : " + checkPalindrome(num));
        sc.close();
    }
}
```

```cpp
#include <iostream>
#include <cstring>
using namespace std;
string checkPalindrome(int a)
{
    int pal = 0, n;
    int original = a;
    while (a > 0)
    {
        n = a % 10;
        pal = pal * 10 + n;
        a = a / 10;
    }
    if (original == pal)
    {
        return "Palindrome number";
    }
    return "Not palindrome number";
}

int main()
{
    int num;
    cout << "Input  : ";
    cin >> num;
    cout << "Output : " << checkPalindrome(num) << endl;
    return 0;
}
```

```c
#include <stdio.h>
char *checkPalindrome(int a)
{
    int pal = 0, n;
    int original = a;
    while (a > 0)
    {
        n = a % 10;
        pal = pal * 10 + n;
        a = a / 10;
    }
    if (original == pal)
    {
        return "Palindrome number";
    }
    return "Not palindrome number";
}
int main()
{
    int num, b = 0;
    printf("Input  : ");
    scanf("%d", &num);
    printf("Output : %s\n", checkPalindrome(num));
    return 0;
}
```

</CodeBlock>
