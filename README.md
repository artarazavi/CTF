# Reverse Engineering CTF challenge 
**challenge based on MAC OS architechture**   
Must have [radare2](https://github.com/radareorg/radare2) installed to run this
```
$ brew install radare2
```
Clone this repo enter into the folder and run
```
$ r2 crackme[#]
-- [some radare2 fortune for fun]
```
fun note: radare will tell you a fortune when you open up the file. to get another fortune simply run the "fo" command.   
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