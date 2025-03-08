# PicoCTF Notes
## Level: Tab, Tab, Attack

For this level we're given a folder called `Addadshashanammu`

Inside this folder there are a few more sub-folders which we can quickly jump into using `cd` + `TAB` for autocompleting

Finally we see a file called `fang-of-haynekhtnamet` 

Running:
```bash
file fang-of-haynekhtnamet

fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=e34ce4e4ee2f7ce7fb251c8f5ab036da9882bc55, not stripped
```
We can see it's a binary executable. Assuming that the flag is probably inside this file

We can run the following to extract the flag
```bash
strings fang-of-haynekhtnamet | grep "pico"
```
* The `strings` command is used to search for printable strings within a binary file
* We then pipe the output to `grep` where we search for the string `"pico"` in order to extract the line with the flag

## Flag:
``` picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4} ```