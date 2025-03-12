# PicoCTF Notes
## Level: Python Wrangling

For this level we're given:
- A python file `ende.py`
- An encrypted txt file with the flag `flag.txt.en`
- A txt file containing a password `pw.txt`

Looking at the src code for `ende.py` we can see that it's used to either encrypt or decrypt file using the `-e` or `-d` flag

Running the file to decrypt the `flag.txt.en` gives us the flag

```bash
python ende.py -d flag.txt.en

# Running this prompts us for the password which we can find in pw.txt
```


## Flag:
``` picoCTF{4p0110_1n_7h3_h0us3_6008014f} ```