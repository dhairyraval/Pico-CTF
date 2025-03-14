# PicoCTF Notes
## Level: Codebook

For this level we're given:

* A python script `code.py`
* A text file `codebook.txt`

Running `code.py` with `codebook.txt` in the same folder gives us the flag

### Logic
The `code.py` contains a `XOR` encryption/decryption function which can be used to encrypt/decrypt text along with a key

* The encrypted flag is already hard coded in `code.py` and we get the key from `codebook.txt`


## Flag:
``` picoCTF{c0d3b00k_455157_7d102d7a} ```