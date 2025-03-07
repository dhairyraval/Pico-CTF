# PicoCTF Notes
## Level: Glitch Cat

For this level we need to connect to a nc listener at:
`nc saturn.picoctf.net 55374`

Here we see the following text:

```bash
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
```

Getting the ASCII values for the 2nd part of the flag that's being represented as a concatenation of __hex values__  gives us the complete flag!

## Flag:
``` picoCTF{gl17ch_m3_n07_bda68f75} ```