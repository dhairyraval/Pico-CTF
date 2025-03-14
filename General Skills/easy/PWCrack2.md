# PicoCTF Notes
## Level: xxxx

This level is similar to `PWCrack1`

We're given the encrypted flag `level2.flag.txt.enc` and a password checker `level2.py`

Again we just need to run `level2.py` and provide it with the valid password

* Looking at the src code, we can see that the password is:
    ```python
    chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)
    ```

* The password is represented as a concatenation chars represented by their __hexadecimal ASCII values__

* I just asked chatGPT to give me the ASCII string - `4ec9`

## Flag:
``` picoCTF{tr45h_51ng1ng_9701e681} ```