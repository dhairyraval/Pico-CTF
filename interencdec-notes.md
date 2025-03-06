# PicoCTF Notes
## Level: interencdec

This level is a basic intro to cryptography

We're given a file - `enc_flag`

Opening the file we see the following text:

```
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6YzRNalV3YUcxcWZRPT0nCg==
```

* The `==` can be a hint that it's encoded in base64

Decoding with base64 gives us:

```bash
cat enc_flag | base64 -d
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaG1qfQ=='
```

* We can remove the leading "b" and surrounding quotes 
  * The motivation behind this is that the `b''` notation appears when printing bytes objects in python - so removing the `b''` will give us thea actual base64 string

Decoding again:
```bash
echo "d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaG1qfQ==" | base64 -d
wpjvJAM{jhlzhy_k3jy9wa3k_78250hmj}
```

The text `wpjvJAM{jhlzhy_k3jy9wa3k_78250hmj}` looks to be in the format of `picoCTF{somelevel_flag}`

* We can decoding using ROT7 (Ceasar Cipher), which gives us the flag!
* I just used an online tool for this, too lazy to write a command for it.


## Flag:
``` picoCTF{caesar_d3cr9pt3d_78250afc} ```