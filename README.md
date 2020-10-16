
# CONTENTS OF THIS FILE
---
 * **Introduction**
 * **Contributurs**
 * **Libraries**
 * **Making an ".exe" file**
 * **How the program runs**
 * **How to run** 
 * **Refrences**
  
---
## INTRODUCTION
----
---

> Rotor machine cipher uses two cylinders to change the order of the characters to encrypt. The inner cylinder turns after typing one character, and the outer one changes after 26 rotation of the inner rotary. The cylinders have two columns with random digits. First, each typed character represents a number of the first column of the fast cylinder. Then, that number finds itself on the second column and points to the corresponded one on the outer router. After finding itself on the second column of the slower rotary, that number shows a ciphered character.  

---                

## CONTRIBUTURES
---
---
| Name                 | Email                 |
| -------------------- | ----------------------|
| Reza Aliyari         | *<raliyari@nyit.edu>* |
| Ali Azizpour         | *<aazizpou@nyit.edu>* |
| Raheleh Sheikhansari | *<rsheikha@nyit.edu>* |

---
## LIBRARIES 
---
---
* System;
* System.Collections;
* System.Collections.Generic;
* System.Linq;
---
## MAKING AN ".EXE" FILE
---
---
> Using Mono is a practical way To creat an .exe file for Windows. 
>
>1. First, download the Mono binaries, and type the following commands to configure it :

```bash
wget --no-check-certificate http://raw.github.com/nathanb/iws- snippets/master/mono-install-scripts/ubuntu/install_mono-3.0.sh
chmod 755 install_mono-3.0.sh
./install_mono-3.0.sh
```

>2. Then, install the the MCS package:
```bash
sudo apt-get install mcs
```
>3. After that, compile your program:
```bash
mcs program.cs
ls
program.cs program.exe
```
>4. Finally, run the program:
```bash
./program.exe
```
---
## HOW THE PROGRAM WORKS
---
---
> This program contains three functions: refill, shift forward, and main. The main class uses those two others. 
>
> * **Shift forward class:** It takes a list of cylinders called “lst.” There is a temp list named “templst,” which includes the final input list of “lst” in the body. Then, a for ring gets other inputs and fills the “templst”.
>
>* **Refill class:** After taking an input list, it uses the “random” function to create random numbers between 1 to 27 and adds to the input list, which is the cylinder. If the input were equal to 26, it would exit from the while loop.
>
>* **Main class:** First, it refills cylinder1,2. Then, it prints their initial output strings.

>It is used a do-while loop for the main part, and it exits by pressing the “**Esc**” key.
It asks the input character, by “*Console.ReadKey()*".
There are three "If loop" in this part:
>
>1. **Initial If:** 
>
>    * First, it shifts the cylinder1 and shows the contents. 
>    * Then, it goes to the “relation” loop to find the relationship between the two cylinders and the output.
>    * As the characters are constant in both cylinders and just the indexes change, to create "colFisrt," the index part's current character hints its number in the first cylinder's first column. After that, it finds the same digit on the second column. Next, it looks for the represented index in the first column of the second cylinder. Finally, it searches itself on the second column of the second cylinder.
>2. **Second If:**
>    * After completing the input text, press "Enter", then the ciphered text will appear. Also, it exits from the program by pressing the "exit" button.
>3. **Third If:**
>    * Symbols, numeric, spaces and special characters should not be encrypted. Also, it converts input text in lower case.
---

## HOW TO RUN
---
---

> The example below shows how this code works:  
> It is written, "Press key is:" that asks the string to encrypt. After completing the text, press "**Enter**", then the ciphered text will appear:

```c#
Press Key is: cryptography
Converted Keys is: fenlgffqjvvd
```
> Each letter will never convert to itself, and because of cylinders' rotation, the last encrypted text does not repeat.

```c#
Press Key is: cryptography
Converted Keys is: pdzilcchnfcc
```
>It exits by pressing the “**Esc**” key. To show the current situation of two cylinders, type the word "**print**".
```c#
Press Key is: print
----------------shifted cylinder1--Inner Cylinder---------------------
[alph A 22 : 15][alph B 23 : 4][alph C 24 : 9][alph D 25 : 17][alph E 26 : 26][alph F 1 : 20][alph G 2 : 3][alph H 3 : 13][alph I 4 : 8][alph J 5 : 18][alph K 6 : 23][alph L 7 : 6][alph M 8 : 2][alph N 9 : 11][alph O 10 : 16][alph P 11 : 25][alph Q 12 : 21][alph R 13 : 5][alph S 14 : 14][alph T 15 : 10][alph U 16 : 19][alph V 17 : 24][alph W 18 : 7][alph X 19 : 12][alph Y 20 : 22][alph Z 21 : 1]
---------------shifted cylinder2--Outer Cylinder--------
[alph A 1 : 26][alph B 2 : 22][alph C 3 : 5][alph D 4 : 1][alph E 5 : 10][alph F 6 : 19][alph G 7 : 15][alph H 8 : 25][alph I 9 : 8][alph J 10 : 4][alph K 11 : 13][alph L 12 : 9][alph M 13 : 18][alph N 14 : 23][alph O 15 : 6][alph P 16 : 16][alph Q 17 : 11][alph R 18 : 21][alph S 19 : 17][alph T 20 : 14][alph U 21 : 24][alph V 22 : 3][alph W 23 : 7][alph X 24 : 12][alph Y 25 : 20][alph Z 26 : 2]
```
---
**To see this Readme file on Github click [here](https://github.com/rahele157/README1/blob/main/README.md).**

## REFRENCES
---
---
* *https://www.tutorialspoint.com/executing-chash-code-in-linux*
* *https://www.youtube.com/watch?v=HUBNt18RFbo&list=PL4lCA8BnLs5c-C1SkVlUf2F0yjaZEk504&index=2*
* *https://www.youtube.com/watch?v=UKbP3Rjxhy0*
* https://stackoverflow.com/questions/18180958/does-code-exist-for-shifting-list-elements-to-left-or-right-by-specified-amount
* https://stackoverflow.com/questions/2706500/how-do-i-generate-a-random-int-number
