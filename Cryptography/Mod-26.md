# PicoCTF Notes
## Level: Mod 26

For this level we need to decrypt the following line of text:

`cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_uJdSftmh}`

Looking at the description we can see that it's encrypted using ROT 13

ROT 13 is a special case of Caesar Cipher where the each letter of a string is shifted by a fixed amount of 13.

I used ChatGPT to decrypt ROT 13, alternatively we can use online tools like this [ROT13 Decoder](https://cryptii.com/pipes/rot13-decoder) by cryptii


## Flag:
``` picoCTF{next_time_I'll_try_2_rounds_of_rot13_hWqFsgzu} ```