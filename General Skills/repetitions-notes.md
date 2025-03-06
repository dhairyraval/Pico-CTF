# PicoCTF Notes
## Level: repetitions

For this level we're given: 
* a file - `enc_flag`
* hint: Multiple decoding is always good

Looking at the hint - this is probably another level with a combination of enocoding methods used on the flag

Viewing the contents of the file we can see that's probably base64 encoded

Decoding the contents once - gives another base64 encoded string as output - so I decided to keep decoding until we get a different output

Running:
```base64
cat enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
```
Gives us the flag!


## Flag:
``` picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_73494190} ```