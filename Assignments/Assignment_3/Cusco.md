# Microcorruption BE & RE

Author: [Akash Biswas](https://github.com/akashkb-a01)

Level Name: Cusco

## Walkthrough
1. Like Hanoi, this problem too insisted on putting passwords between 8-16 characters.
2. So I entered `testtesttesttestt` and got a message saying `insn address unaligned` and also `sp` pointed to `t`(the last one).
3. I read abou it more on the internet and concluded that because returning to address `7400` was not valid as, it was not a valid address.
4. To solve the problem, we must go to `<unlock_door>` at `4446`. So, we must create a password where last two characters should correspond to `0x4446`.
5. Also keeping in mind the endian, I tried `testtesttesttestFD` as `FD` is equivalent to `4644`.

## Password
`testtesttesttestFD`
