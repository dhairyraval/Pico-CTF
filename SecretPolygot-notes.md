# PicoCTF Notes
## Level: Secret of the Polyglot

### This level focuses on forensics and gives an intro to file steganography

For this level we are given a file - `flag2of2-final.pdf`

Opening the file with a pdf view get the following string:
`_1n_pn9_&_pdf_90974127}`

Looking at the hints mentioned in the challenge description - We should try opening the file in other ways

Running:

```bash
file flag2of2-final.pdf
```

Shows us that the file contains PNG image data

Renaming the file to `flag2of2-final.png` and opening it with an image viewer gives us another string:

`picoCTF{f1u3n7_`

Combining both of the strings we found gives us the flag!


## Flag:
``` picoCTF{f1u3n7_1n_pn9_&_pdf_90974127} ```