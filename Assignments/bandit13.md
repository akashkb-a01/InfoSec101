# Bandit Level 13 to 14 Writeup


Author: [Akash Biswas](https://github.com/akashkb-a01)

Problem Page: [bandit13](https://overthewire.org/wargames/bandit/bandit14.html)

## List of Commands Used
```
ls - list files in a directory
ssh - OpenSSH SSH client (remote login program)
cat - concatenate files and print on the standard output

```

## Walkthrough
After going through reading material, I felt that it has to be done using ssh command. So, I went through the man page of ssh and figured out -i. After login I just had to access the file located at /etc/bandit_pass/bandit14. 

## Password
`4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e`

## Bash/Python script to automate the process
```
#!/bin/expect -f
spawn ssh bandit13@bandit.labs.overthewire.org -p 2220
expect "password: "
send "8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL\r"
expect "$ "
send "ls\r"
expect "$ "
send "ssh -i sshkey.private bandit14@localhost\r"
expect "? "
send "yes\r"
expect "$ "
send "cat /etc/bandit_pass/bandit14\r"
expect "$ "
send "exit\r"

```
