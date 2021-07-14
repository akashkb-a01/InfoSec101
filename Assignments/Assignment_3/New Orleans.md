# Microcorruption BE & RE

Author: [Akash Biswas](https://github.com/akashkb-a01)

Level Name: New Orleans

## Walkthrough
1. In this level, first the password will be created. Then it will get the password from the user and compare them.
2. So, I set a breakpoint at `<check_password>` and entered some random password `test`.
3. Inside `<check>_password>` at `44c2`, it compared values at memory locations `439c`(our input) and `2400`(password).
4. If the values do not match, in the next step, we get redirected to `44d2` clearing `r15`(where password is stored).
5. So, we note the value at `2400`(`4gu<+tt` in my case) and input it as password after resetting the CPU.

## Password
`4gu<+tt`
