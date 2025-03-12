# PicoCTF Notes
## Level: Static ain't always noise

For this level we're given:

- A binary file `static`

- A bash script `itdis.sh`

We need to find flag from tthe given binary - looking at the level description we can use the bash script to extract readable strings from `static`

### Solution

There are 2 ways to solve this level (that I know of)

* __The Intended Way__
    * Running: 
    ```bash
    ./ltdis.sh static
    ```
    and getting the flag from the `static.itdis.strings.txt` file that's created


* __Quicker way__
    * A faster way to get the flag is to extract the readable strings from the binary using `strings` and pipe the output to `grep`

    ```bash
    strings static | grep "pico"
    ```


## Flag:
``` picoCTF{d15a5m_t34s3r_1e6a7731} ```