# PicoCTF Notes
## Level: endianness

This level introduces the concept of Endian Representaion, and how it's used to store data which is mutiple bytes in size

We're given a random word: **"plpmf"** and we need to find it's little and big endian representations in order to get the flag for the level

## Commands Ran:
```bash
#little endian:
echo "plpmf" | xxd -e

#big endian:
echo -n "plpmf" | xxd -g 1
```
* Note: The outputs just need to be lightly formatted (removing spaces, etc.)

## Flag:
``` picoCTF{3ndi4n_sw4p_su33ess_91bc76a4} ```