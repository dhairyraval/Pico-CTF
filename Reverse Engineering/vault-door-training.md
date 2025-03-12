# PicoCTF Notes
## Level: vault-door-training

For this level we're given a file `VaultDoorTraining.java`

With the following function present in the file:

```java
// The password is below. Is it safe to put the password in the source code?
// What if somebody stole our source code? Then they would know what our
// password is. Hmm... I will think of some ways to improve the security
// on the other doors.
//
// -Minion #9567
public boolean checkPassword(String password) {
    return password.equals("w4rm1ng_Up_w1tH_jAv4_be8d9806f18");
}
```
* From this function we can get the password string - `w4rm1ng_Up_w1tH_jAv4_be8d9806f18`

This is flag!

## Flag:
``` picoCTF{w4rm1ng_Up_w1tH_jAv4_be8d9806f18} ```