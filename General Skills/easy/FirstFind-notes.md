# PicoCTF Notes
## Level: First Find

For this level we need to find a particular file `uber-secret.txt` from a given folder `files`

Using the `find` command we can get the location for the file and then `cat` the contents of the file to get the flag!

```bash
cat "$(find . -type f -name "uber-secret.txt")"
```

## Flag:
``` picoCTF{f1nd_15_f457_ab443fd1} ```