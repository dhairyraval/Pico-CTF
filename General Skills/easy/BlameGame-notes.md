# PicoCTF Notes
## Level: Blame Game

This level is another basic intro to git

For this level we're given a file called `message.py` and we need to find the user who's commit is preventing the program from runnning

Using:
```bash
git log -p message.py
```

We can view the history of all commint on the file and here we can find the name of the user (which is the flag)

## Flag:
``` picoCTF{@sk_th3_1nt3rn_cfca95b2} ```