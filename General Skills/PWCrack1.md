# PicoCTF Notes
## Level: PW Crack 1

For this level we're given:

* A password checker - `level1.py`

* An encrypted flag - `level1.flag.txt.enc`

Running the `level1.py` we are asked for a valid password
  * If we take a look at the src code of `level1.py` we can see that the valide password is `8713`
  * Entering the valid password prints the flag


## Flag:
``` picoCTF{545h_r1ng1ng_1b2fd683} ```