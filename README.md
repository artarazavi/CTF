# Reverse Engineering CTF challenge 
** challenge based on MAC OS architechture   
Must have radare2 installed to run this   
Clone this repo and run
```
$ r2 crackme[#]
```
When the radare prompt opens up run the "aa" command to analyze the code.   
Then run the seek command "s main" to jump to the main section of the code.   
Then run the "VV" command to switch to visual graph mode.