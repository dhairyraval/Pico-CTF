# PicoCTF Notes
## Level: WebDecode

For this level we need to find the flag from the src code of the given website

Inspecting all the pages on the website - we can see a section container like this:

` <section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMjgzZTYyZmV9"> `

The string set for `notify_true` looks like it's probably base64 encoded - decoding it give us the flag!


## Flag:
``` picoCTF{web_succ3ssfully_d3c0ded_283e62fe} ```