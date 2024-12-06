# <p align="center">GOOD CODE</p>

In this file I try to save good code I acquire throughout my journey

## Rock paper scissors the smart way, Python:

```python
def rps(p1, p2):
    beats = {'rock': 'scissors', 'scissors': 'paper', 'paper': 'rock'}
    if beats[p1] == p2:
        return "Player 1 won!"
    if beats[p2] == p1:
        return "Player 2 won!"
    return "Draw!"
```
## Rot 13:
Rot13 is a simple letter substitution cipher that replaces each letter with the letter 13 positions ahead of it in the alphabet. In other words, it's a Caesar cipher with a shift of 13. For example, the letter "a" becomes "n", "b" becomes "o", and so on. This means that if you have a message that uses only letters, you can easily decode it by shifting each letter back 13 positions.

<center>
  <img src="assets/caesar_cipher.gif" alt="Caesar cipher image" style="width: 400px; height: 400px; margin: 0 auto; display: block;">
</center>

```python
import string
def rot13(message):
    lc = string.ascii_lowercase #lc stands for "lowercase characters"
    uc = string.ascii_uppercase #uc stands for "uppercase characters"
    res = ""
    for c in message: #Looping through the given string
        if c in lc:
            res += lc[(lc.index(c) + 13) % 26] #Adding the 13th letter ahead of c to the result variable, if c is lowercase.
        elif c in uc:
            res += uc[(uc.index(c) + 13) % 26] #Adding the 13th letter ahead of c to the result variable, if c is uppercase.
        else:
            res += c #If c is not in lc nor uc it will be added to the result with no modification
    return res
```

## Clear screen func:
A func that can be added to a python script, especially python CLI apps, for all OSs.
```python
import os
def clear_screen():
    # For Windows
    if os.name == 'nt':
        _ = os.system('cls')
    # For Mac and Linux
    else:
        _ = os.system('clear')
```

## A clever kata solution:
The problem:  

> In this kata you are required to, given a string, replace every letter with its position in the alphabet. If anything in the text isn't a letter, ignore it and don't return it.

The clever [solution](https://www.codewars.com/kata/reviews/546f92300e7b08fe6100001c/groups/546f995f304c12f1e00002b2):

```python
def alphabet_position(text):
    return ' '.join(str(ord(c) - 96) for c in text.lower() if c.isalpha())
```