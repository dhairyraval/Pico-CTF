# PicoCTF Notes
## Level: strings it

For this level we're given a file __strings__ and we need to find the flag from this file 

Using the `strings` command we can extract all readable strings from the given file and pipe the output to `grep` to print the line containing the flag

```bash
strings strings | grep "pico"
```

## Flag:
``` picoCTF{5tRIng5_1T_7f766a23} ```