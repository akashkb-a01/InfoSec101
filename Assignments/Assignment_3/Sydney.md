# Microcorruption BE & RE

Author: [Akash Biswas](https://github.com/akashkb-a01)

Level Name: Sydney

## Walkthrough
1. In this level, the entered password will be stored at `r15` or `439c` in memory dump.
2. It will then check the password using `<check_password>`. So, I entered some random password `test` setting a breakpoint at `<check_password>`.
3. Inside `<check>_password>`, it compared values at memory `r15`(first two characters) and `0x5937`.
4. So, I entered the password as `5937` after resetting checking the option if entered value was hex-encoded.
5. But still it did not work. Afterwards, I got my mistake, as I did not checked the endian.
6. So, I entered password as `3759` which did the work. Similarly I did it for next six characters and got password as `3759422f6b632c47` equivalent to `7YB/kc,G`.

## Password
`7YB/kc,G`
