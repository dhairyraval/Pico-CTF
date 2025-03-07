# PicoCTF Notes
## Level: HashingJobApp

For this level we need to connect to a nc listener at: `nc saturn.picoctf.net 59327`

Here we see that we need to get the md5 hash of the given strings

We can get that using:

```bash
echo -n "<given-string>" | md5sum
```
* Basically we're echoing the given string and piping the output to `md5sum` command to get the md5 hash of the string

We need to do this 4 times and then we get the flag!

## Flag:
``` picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02} ```