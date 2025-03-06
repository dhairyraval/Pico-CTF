# PicoCTF Notes
## Level: Collaborative Development

This level gives a basic intro to merging different branches on git and resolving merge conflicts

We're given a git repo with 3 local branches and we need to merge all 3 to main and resolve any merge conflicts to get the flag

Not adding detailed step-by-steps for this one.

## Commands used:
```bash
git branch -a  # to list all branches

git merge <branch-name> # merge <branch-name> with current branch

git add .;git commit -m  # Add & commit changes after resolving merge conflicts
```

## Flag:
``` picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_e4b79efb} ```