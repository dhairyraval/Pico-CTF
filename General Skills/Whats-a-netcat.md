# PicoCTF Notes
## Level: what's a net cat?

This level is an intro tothe `netcat` command 

In order to get the flag we need to connect to __jupiter.challenges.picoctf.org__ at port __25103__

Running the following `nc` command let's us connect to the target at the given port:

```bash
nc jupiter.challenges.picoctf.org 25103
```


## Flag:
``` picoCTF{nEtCat_Mast3ry_d0c64587} ```