# Reverse Engineering CTF challenge 
A series of reverse engineering puzzles of increasing complexity.
## Purpose
This CTF challenge focuses on strengthening the user’s reverse engineering abilities through solving a series of increasing complexity puzzles. Reverse engineering is an important first step in malware analysis because when malware is discovered on a machine it is in binary format. The only way to figure out how the attack took place and which vulnerabilities were exploited is through deciphering the binary code. This is a challenge aimed mostly at beginners and one does  not need previous assembly programming experience to complete it. 
## Install radare2
Must have [radare2](https://github.com/radareorg/radare2) installed to run this
```
$ brew install radare2
```
## How to run CTF challenge
**challenge based on macOS architechture**   
Clone this repo enter into the appropriate folder and run
```
$ r2 crackme[#]
-- AHHHHH!!!! ASSEMBLY CODE!!!!!! HOLD ME I'M SCARED!!!!!!!!!![some radare2 fortune]
```
fun note: radare will tell you a fortune when you open up the file. To get another fortune simply run the "fo" command.   
When the radare prompt opens up run the "aa" command to analyze the code.
```
[0x100000e80]> aa
[x] Analyze all flags starting with sym. and entry0 (aa)
```
Then run the seek command "s main" to jump to the main section of the code.
```
[0x100000e80]> s main
``` 
Then run the "VV" command to switch to visual graph mode.
```
[0x100000e80]> VV
```
To quit radare simply hit 'q' twice while in graph mode to get back to the prompt and then run the "quit" command.
```
[0x100000e80]> quit
```

## Build your own C binary output file for radare2
Create a C file of your choice and run
```
$ gcc -o crackme crackme.c
```
Then you can input the binary file into radare2
```
$ r2 crackme
-- [some radare2 fortune]
```