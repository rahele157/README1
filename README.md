
# CONTENTS OF THIS FILE
---------------------

 * **Introduction**
 * **Contributurs**
 * **Making an ".exe" file**
 * **How to run** 
 * **Refrences**
  

## INTRODUCTION
-------

Rotor machine cipher uses two cylinders to change the order of the characters to encrypt. The inner cylinder turns after typing one character, and the outer one changes after 26 rotation of the inner rotary. The cylinders have two columns with random digits. First, each typed character represents a number of the first column of the fast cylinder. Then, that number finds itself on the second column and points to the corresponded one on the outer router. After finding itself on the second column of the slower rotary, that number shows a ciphered character.  

---
## CONTRIBUTURES
----------------------

* Reza Aliyari *<raliyari@nyit.edu>*
* Ali Azizpour *<aazizpou@nyit.edu>*
* Raheleh Sheikhansari *<rsheikha@nyit.edu>*

---
## MAKING AN ".EXE" FILE
-----------------------
Using Mono is a practical way To creat an .exe file for Windows. 
1. First, download the Mono binaries and to configure it type the following commands:
```
wget --no-check-certificate http://raw.github.com/nathanb/iws- snippets/master/mono-install-scripts/ubuntu/install_mono-3.0.sh
chmod 755 install_mono-3.0.sh
./install_mono-3.0.sh
```
2. Then install the the MCS package:
```
sudo apt-get install mcs
```
3. After that, compile your program:
```
mcs program.cs
ls
program.cs program.exe
```
4. Finally, run the program:
```
./program.exe
```
---

## HOW TO RUN
--------------------

The example below shows how this code works:
By typing any character, the ciphered letter appears simultaneously. 

```
Press Key is: cryptography
Converted Keys is: LHVTMGIPIJCQ
```
Each letter will never convert to itself, and because of cylinders rotation the previous encrypted text does not repeat.

```
Press Key is: cryptography
Converted Keys is: QZOMPZXYFZEP
```

After 26 letters the outer cylinder clicks once.
It is clear that symbols, numeric, spaces, and special characters should not be encrypted. Also, it converts input text in lower case.
```
Press Key is: "Mr. Jock, TV quiz PhD, bags few 1ynx"
Converted Keys is: "GU. GUQL, UQ PAEI DCP, KKDO OOV 1JQA"
----------------shifted cylinder1-----------------------
[alph A 2 : 2][alph B 3 : 11][alph C 4 : 20][alph D 5 : 16][alph E 6 : 25][alph F 7 : 21][alph G 8 : 5][alph H 9 : 14][alph I 10 : 10][alph J 11 : 19][alph K 12 : 24][alph L 13 : 7][alph M 14 : 3][alph N 15 : 12][alph O 16 : 22][alph P 17 : 17][alph Q 18 : 1][alph R 19 : 15][alph S 20 : 4][alph T 21 : 9][alph U 22 : 18][alph V 23 : 23][alph W 24 : 26][alph X 25 : 8][alph Y 26 : 13][alph Z 1 : 6]

---------------shifted cylinder2-----------------------
[alph A 2 : 2][alph B 3 : 11][alph C 4 : 20][alph D 5 : 16][alph E 6 : 25][alph F 7 : 21][alph G 8 : 5][alph H 9 : 14][alph I 10 : 10][alph J 11 : 19][alph K 12 : 24][alph L 13 : 7][alph M 14 : 3][alph N 15 : 12][alph O 16 : 22][alph P 17 : 17][alph Q 18 : 1][alph R 19 : 15][alph S 20 : 4][alph T 21 : 9][alph U 22 : 18][alph V 23 : 23][alph W 24 : 26][alph X 25 : 8][alph Y 26 : 13][alph Z 1 : 6]
```
----

## REFRENCES
---
* *https://www.tutorialspoint.com/executing-chash-code-in-linux*
* *https://www.youtube.com/watch?v=HUBNt18RFbo&list=PL4lCA8BnLs5c-C1SkVlUf2F0yjaZEk504&index=2*
* *https://www.youtube.com/watch?v=UKbP3Rjxhy0*
