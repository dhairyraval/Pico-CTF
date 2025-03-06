# PicoCTF Notes
## Level: CanYouSee

For this level we're given a `.jpg` image file

Looking at the hints of the level, we get an idea that the flag is probably hidden somewhere in the metadata of the image file

Using `exiftool` we can view detailed info about the meta datat

```bash
exiftool <img-name>
```
* In the results, the Attribution URL feild stand out as it contains a base64encoded string - why would this feild need encoded data?

Decoding using base64 gives us the flag!
```bash
echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg==" | base64 -d
picoCTF{ME74D47A_HIDD3N_6a9f5ac4}
```

## Flag:
``` picoCTF{ME74D47A_HIDD3N_6a9f5ac4} ```