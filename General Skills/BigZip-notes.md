# PicoCTF Notes
## Level: Big Zip

For this level we're given a folder `big-zip-files`

Inside of this folder we have many sub-folders and inside of these sub-folders we have many `.txt` files

Looking at the challenge description we know that that flag is present in one of these `.txt` files

Running the following `grep` command (from inside `big-zip-files`) gives us the flag:

```bash
grep -r -n "picoCTF{" . --include="*.txt"
```
### Logic
* The `grep` command is recursively search through the present directory `.`
* We're searching for a string matching: `"picoCTF{"`
* ___optional___: the `include` flag is optional as all the files inside all the sub-directories are `.txt` anyway

## Flag:
``` x ```