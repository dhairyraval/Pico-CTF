# PicoCTF Notes
## Level: First Grep

This level is an intro to the `grep` command 

We're given a file called `file` which contains a lot of random text

We need to find the flag from the text in the file

Running `grep` gives us the flag:

```bash
grep "picoCTF{" file

#this command search the contents of the file for the matching string "picoCTF{" and prints each line containing the matching string
```

## Flag:
``` picoCTF{grep_is_good_to_find_things_dba08a45} ```