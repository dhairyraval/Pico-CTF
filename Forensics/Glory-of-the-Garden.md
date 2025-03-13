# PicoCTF Notes
## Level: Glory of the Garden

For this level we're given a `garden.jpg` image file and we need to find the flag from this file

Looking at the hint - "What is a hex editor?"

* I decided to use `xxd` to try and see if the flag is hidden in the hex dump of the __garden.jpg__ file

    * `xxd` is used to the hexdump (or the byte-by-byte) representation of a file's raw data


* Here's the command I used:

```bash
#Piping the output from xxd to cut for better formating - this way only see the ASCII part in the output
 xxd garden.jpg | cut -c 50- 
```

* Another easier way to get the flag is to use the `strings` command and pipe the result to `grep`

```bash
strings garden.jpg | grep "pico"
```

## Flag:
``` picoCTF{more_than_m33ts_the_3y3eBdBd2cc} ```