# PicoCTF Notes
## Level: Transformation

For this level we have to decrypt the given text in a `enc` file to get the flag

Looking at the level description we get the method for encoding used:

```python
''.join(
        [chr((ord(flag[i]) << 8) + ord(flag[i + 1])) 
            for i in range(0, len(flag), 2)
        ]
    )
```

* The logic is that each letter is being shifted by 8 bits to the left and then the 2nd letter is being added to the encoded string

Used the following python script from [this](https://medium.com/@CYberVIaz/pico-ctf-transformation-writeups-a5496cb3377b) writeup by CYber VIaz

```python

word = "<encoded text from the enc file>"
flag = ""

for i in range(0, len(word)):
    flag += chr(ord(word[i]) >> 8)
    flag += chr(ord(word[i]) - (ord(flag[len(flag)-1]) << 8))

print(flag)

```

## Flag:
``` picoCTF{16_bits_inst34d_of_8_e141a0f7} ```