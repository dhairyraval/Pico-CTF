# PicoCTF Notes
## Level: Wave a flag

For this level we're given a file called `warm` which is a binary executable

All we need to do is add execute permissions - `chmod +x <filenmae>`

And then execute it while giving it the `-h` flag

```bash
./warm -h
```

## Flag:
``` picoCTF{b1scu1ts_4nd_gr4vy_f0668f62} ```