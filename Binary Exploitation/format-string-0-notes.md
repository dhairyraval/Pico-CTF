# PicoCTF Notes
## Level: format string 0

This level is a **Binary Exploitation** challenge where we use **format specifiers** to exploit a vulnerable binary file.


## Source Code Analysis
Looking at the provided source code, we see that `serve_patrick()` is called from `main()`.

### Exploiting `serve_patrick()`
For this function, we need the `count` variable to be **greater than `2 * BUFSIZE`**.  
The only input that works is:

```
Gr%114d_Cheese
```

This works because the `%114d` format specifier adds a minimum **114 field width** to the character,  
causing `count` to become **114**, which satisfies the condition `if (count > 2 * BUFSIZE)`.

---

### Exploiting `serve_bob()`
For the next function, we need to pick the option:

```
Cla%sic_Che%s%steak
```

This works because the `%s` format specifier in the input will try to reference a valid string in memory.  
Since there is **no valid string named `'steak'`**, it results in a **segmentation fault (SIGSEGV)**.

---

## Triggering the Flag
The function:

```c
void sigsegv_handler(int sig)
```
is present in the source code and is invoked when the segmentation fault occurs.  
This function prints the flag for us!

## Flag:
```
picoCTF{7h3_cu570m3r_15_n3v3r_SEGFAULT_a1d85b3e}
```