# PicoCTF Notes
## Level: Bases

For this level we're given a random text `bDNhcm5fdGgzX3IwcDM1`

and given the hint that "it has something to do with bases"

Taking a closer look at the given text - it seems it's probably base64 encoded and we need to decode it and convert the binary to ascii to get the flag

* There are several ways to convert base64 to ascii - online tools, cmd line tools, chatGPT, etc.

* I used [CyberChef](https://gchq.github.io/CyberChef/) to get the flag as ascii text: `l3arn_th3_r0p35`

## Flag:
``` picoCTF{l3arn_th3_r0p35} ```