# PicoCTF Notes
## Level: Scan Surprise

For this level, we are given:

- `flag.png` - an image file containing a **QR code**.

Reading the level description, we know that this image file contains the flag encoded as a QR code.

## Extracting the Flag

Running the following command:

```
zbarimg flag.png
```

This extracts and gives us the flag!

## Flag:
```
picoCTF{p33k_@_b00_b5ce2572}
```