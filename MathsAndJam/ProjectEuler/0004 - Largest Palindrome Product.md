---
date: 2026-03-19
tags:
  - projecteuler
  - palindromes
  - products
eulertime: 0.101
---

# Problem:

A palindromic number reads the same both ways. The largest palindrome made from the product of two $2$-digit numbers is $9009 = 91 \times 99$.

Find the largest palindrome made from the product of two $3$-digit numbers.

# Solution: 906609

```
def products (first=999,second=999):  
    palindromes = []  
    while first >= 10:  
        second_reset=second  
        while second_reset >= 10:  
            numb = str(first * second_reset)  
            reverse_numb = numb[::-1]  
            if numb == reverse_numb:  
                palindromes.append(first*second_reset)  
            second_reset -=  1  
        first -= 1  
    print(max(palindromes))  
products()
```

# Commentary:

I'd like to revisit any possible systematic way of targeting the *largest* palindrome rather than cycling from 999 to 1 with the second factor whilst keeping the first at 999, then repeating with the first now at 998, and so on.

It took me a while to understand why I wasn't seeing all possible palindromes, until I asked for the product pairs and saw that the second product wasn't being "reset" to 999 after completing each cycle.
