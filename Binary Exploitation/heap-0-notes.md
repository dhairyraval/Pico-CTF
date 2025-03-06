# PicoCTF Notes
## Level: heap 0

This level is a basic introduction to **heaps** and how **buffer overflows** can be used to change values for neighboring blocks of data.

## Exploitation Process

We are given access to write to a block of data on the heap with  
**address:** `0x5d8fadf5b2b0`

Our goal is to somehow edit the value stored in  
**address:** `0x5d8fadf5b2d0`

### Overflowing the Buffer
If we enter some data **greater than 32 characters** in length, we can overflow the buffer.  
This results in the neighboring block (target block) getting its value **changed**.

## Flag:
```
picoCTF{my_first_heap_overflow_1ad0e1a6}
```
