# Level Name: Verify

## Overview
For this level, we are given the following:

- `checksum.txt` - A text file containing the SHA-256 hash.
- `decrypt.sh` - An executable script that will decrypt the valid file to provide the flag.
- `files/` - A folder containing several files, one of which is the valid file.

## Commands Run
```bash
for file in files/*; do
  sha256sum "$file" | cut -d ' ' -f1 | grep -Fxq -f checksum.txt && echo "Match found - file name: $file"
done
```

## Logic:
- We run the for loop and iterate over all the files in .files
- For each file we first get the checksum using 'sha256sum'
- We extract just the checksum - by using the 'cut command
- This extracteed checksum is then compared with the text in checksum.txt
- If we find a match we get the file name

After this we can simply run `./decrypt.sh files/<file-name>` to get the flag