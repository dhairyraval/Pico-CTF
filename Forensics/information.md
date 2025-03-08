# PicoCTF Notes
## Level: information

For this level we're given a image file `cat.jpg`

The hint for the level mentions that we should take a look at the details for the image

Using `exifTool` to get a detailed info about metadata

```bash
# Showing only the relevant part of the output
exiftool cat.jpg 
...
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
...
```

The license for the image looks to be encoded with base64

Decoding it gives us the flag!

## Flag:
``` picoCTF{the_m3tadata_1s_modified} ```