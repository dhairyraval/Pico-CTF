# PicoCTF Notes
## Level: fixme2.py

Similar to `fixme1` we're again given a python script to fix `fixme2.py`

This time we just need to update an incorrect if statement on line 22

```python
if flag = "" # incorrect

if flag == "" # updating to conditional operator '=='
```

## Flag:
``` picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b} ```