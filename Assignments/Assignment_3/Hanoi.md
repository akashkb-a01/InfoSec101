# Microcorruption BE & RE

Author: [Akash Biswas](https://github.com/akashkb-a01)

Level Name: Hanoi

## Walkthrough
1. In this level, I entered `testtesttest` as password and tracked the whole `<test_password_valid>` function, only to know that it held no significance at `4544` in `<login>`.
2. I noticed that at `455a` in `<login>`, it compared `0x1b` with value stored at `2410` in memory dump. Also if the values did not matched, in next step we would get redirected to end.
3. But value at `2410` was `00` but also it was just after our entered input.
4. So, I tried entering input as `testtesttesttestt` and was surprised to see `74` at `2410`
5. So, finally I tried password as `000000000000000000000000000000001b`(hex encoded) as `1b` is not a readable ASCII character and it worked.

## Password
`000000000000000000000000000000001b`
