# Reverse Engineering CTF challenge 
** challenge based on MAC OS architechture **
Must have [radare2](https://github.com/radareorg/radare2) installed to run this
```
$ brew install radare2
```
Clone this repo and run
```
$ r2 crackme[#]
```
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