# Bandit
```
ssh banditX@bandit.labs.overthewire.org -p 2220
```

#### Level 0

Level 1 Password: `secret CIw56Wxb1myXvJ22NUJjHx9QxUiIbuL6/5kIva7flwaZZBHimYiqYtfE5bIuZuWR+JaNcw5uEMW+Wbgx2Cg8gtJCMnBlT8RXrMoSzRhEhNE=`
#### Level 1

```
cat ./-
```

Level 2 Password: `secret 8+NAHhHeWyA79wWUW9H612SORXLqQMTp2uvRzxtmGaJAeozsKpg64K0VMu4+krr2tWlkJ4YWuXL4z2YHlvp984GDBWg8l7sEFJxWiy44c78=`
#### Level 2

Level 3 Password: `secret CIGSPUx0AV0d6pIaSHB6edDbhf4v2ug8aboTqLGQK+PEatv+2HnEdwJ9c7NpBX/op6y+zNoS0nhiayNGYueX5+sBLhQDplKoIllwznczLx8=`
#### Level 3

Level 4 Password: `secret xc580+4O9EFfn5IIUN9g3q2kqEdyh+7cwunCy6pLIqH2i4ECtvOsMlgMk/8VOep4M7qCcIpMm8I1DxMJnRHkPEfIMKC7Oezz/GX914jSwl0=`
#### Level 4

```
cat ./*
```

Level 5 Password: `secret gbFFh3eO1wH1banqWoVfjLz0LOXac3pwpWtcGsW9s/xAATNOnNPzcnadum5ClRm6FwObemF4iqWuFc+Clrc/FIZDXKSNXP+SlmOaqOoKyxA=`
#### Level 5

list recursive, long, all -> find 1033
```
ls -Rla | grep 1033
```

recursively find `.file2` in current directory and get path of each
```
find . -name .file2 -ls
```

Level 6 Password: `secret Ueavzo5PfLzvMTAsA6IY41IdoZdALQnpyfGeSrDQLZQJqXWMhwewoq+SyOWytPEH3SjXjobNknQqpXgAnMQvPFsHxqnJMlD/GiUKL7CNhBc=`
#### Level 6

```
cd /
```

```
ls -Rla | grep bandit7
```

```
find . -name "bandit7.password" -ls
```

Level 7 Password: `secret Gqq01yOP7bM2ONzMZbh9dlklehJLZoZ3QTR4fZt2Bz8fzaq4Yisza4JBaRHAlEgN6wnTtvPAvmc3CB7BqBOvrl9Sn68MiO4C5zHPKJFZc7o=`
#### Level 7

Find the line with the word "millionth"
```
cat data.txt | grep millionth
```

Level 8 Password: `secret nZeEEwDTzyBiFbjHawlCbYBseU9+J5oFzwc31lzPTYDdVal4jgxRxmDICP+LEDsMwfGy/9aleTilmAmMsOTTGoA3Tv7aEFYyX3xqWAqeeHk=`
#### Level 8

Sort data and print the only line that occurs once
```
cat data.txt | sort | uniq -u
```

Level 9 Password: `secret BaSWCXuTw9FRA8sv5Cfq571W2gdHs9FKrEvKc3GTWMuall6lPGffw2rGqzpTMcD+f9Q92ol1fxUmwaWNRzp1E1dEr0ImaV8MSiddHy539EQ=`
#### Level 9

Show only human-readable strings and find `===`
```
cat data.txt | strings | grep ===
```

Level 10 Password: `secret YZjhgb1qtS1nPu6K0xsqkTWmMThRi7IPD3S+4qPJtgeuMjEacyyWav2jMrlZvj5XhhC3XdJHYXPc4JZxhihhFv3Xo41d8zcivqj+CFK7cpQ=`
#### Level 10

Decode base64
```
base64 -d data.txt
```

Level 11 Password: `secret 2OM4wTnL0LJlosrpXfgFSmZWckpj9U10wm1gNDMUYa5fwYlftoX5OaqYKHNzdOfcLepwZZx13qB+Z1FFK+MaiEcYcRORT4A+NH1gGVmdm+Q=`
#### Level 11

rot13 lower
```
tr 'a-z' 'n-za-m'
```

rot13 UPPER
```
tr 'A-Z' 'N-ZA-M'
```

rot13 all-case
```
tr 'a-zA-Z' 'n-za-mN-ZA-M'
```

```
cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-M'
```

Level 12 Password: `secret RjS3tPr7EYvyKpsj1+AxkECDhuBlvJYy1MrwhxfgFoLMwvmhufsrI7OS7tpo0fJWptjCjify036vjgeybsFFK+l3sHdTvL1L0JFwdijIGH8=`
#### Level 12

Copy file to new temp directory and work in there
```
mktemp -d
```

Reverse hexdump
```
xxd -r data.txt
```

Check file type
```
file [filename]
```

Rename file to appropriate format and decompress
```
gzip -d data.gz
bzip2 -d data.bz2
tar -xzf data.tar.gz
```

Level 13 Password: `secret P68M2YqSieqMfZp1R+KIFMykL3HCvdnLdQT82Y62E9BUFFQQhT+GPxVm2nTrkUZ6ZOfluf9BP7wQsE03D+wSMPZjw9DQEWnm3G+d8m0SqvI=`

#### Level 13

Get the SSH key
```
scp -P 2220 bandit13@bandit.labs.overthewire.org:/home/bandit13/sshkey.private .
```

Remotely copy file containing password as bandit14 (authenticate with SSH key)
```
scp -P 2220 -i sshkey.private bandit14@bandit.labs.overthewire.org:/etc/bandit_pass/bandit14 .
```

Fails due to permissiveness. Reduce permissions and copy again.
```
chmod 700 sshkey.private
```

Level 14 Password: `secret cde9UZ+a3n6UkzQ7TNMXiNMtkqGDUoN3QsP4Ij47jQSymgNmkw47JY0WUPgI4g35ovQudJ8HTvgs8pdmuE2Mrk7w0/klC4VZJG/DCuT/zBs=`

#### Level 14

If you want to see the open ports
```
nmap localhost
```

`telnet` vs `netcat`
- `netcat` sends/receives raw data on the `transport layer`
- `telnet` establishes interactive session on the `application layer`

Connect to localhost on port 30000 and submit password for this level
```
nc localhost 30000
```

Level 15 Password: `secret /brVd4pA5UgOeHMo8WQDvusmk58rx1v2ZRqaSzCOKwhnyF56+HxKz9rpHgYJenSLeFtZUNK9pKsW5fQ0uZt7zMTyUTJIm4YQX11bPENwYLI=`

#### Level 15

`ncat` similar to `nc` but with SSL capability

Connect to localhost through port 30001 using SSL/TLS encryption and submit password
```
ncat --ssl localhost 30001
```

Level 16 Password: `secret 0SvmE24uXA6ju3U0WL5fktTeVH8ioUFG3HQIwf99uB+AG5y0dhrCdCEVKjsBWfl3TddL3ECgn8+KRxa7MDss0A5DPmRcyyguz9mIWZ/lMX4=`

#### Level 16

Run SSL/TLS testing script on ports 31000 to 32000
```
nmap --script ssl-enum-ciphers -p 31000-32000 localhost
```

Submit password to the SSL encrypted port
```
ncat --ssl localhost 31790
```

Level 17 SSH Key
```secret
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
```

#### Level 17

Save key and use it to authenticate into this level
```
ssh -i bandit17.sshkey bandit17@bandit.labs.overthewire.org -p 2220
```

Get difference between files
```
diff [file1] [file2]
```

Level 18 Password: `secret ziXaaZFunlwX9Q3mjnOYXb7gTCzmJHq9pCqPMDfcgKcsNdnRnL2vK1ngnBfREmRRLiiSabWD5m1lAZ7nThc4eb6zEkmOpJ+/oZblHndUHUI=`

#### Level 18

Immediately logged out if login with SSH

Password stored in file `readme` in the home directory, so `secure copy` file
```
scp -P 2220 bandit18@bandit.labs.overthewire.org:/home/bandit18/readme .
```

Level 19 Password: `secret dy6baM7mcyx3oykbekgkJO2UY6vEiPB+zY++7YpStFlpRpvcZ3dyh2baRuBEADLNPy8MgOtElTJEuCbTviDPpla05vd+eutPjkQjx6GGvzI=`

#### Level 19

Run `cat` as bandit20
```
./bandit20-do cat /etc/bandit_pass/bandit20
```

Level 20 Password: `secret wP0dxzD66b7hoUYFP0CADDWYIBu1iL9efIe9vH+zX/nVQ0+F1eZf95r6ZYDmg7zBaBPUommrDKvKf/+6C8DXHFwBiIyu+yUs7xa/D9KCxQ8=`

#### Level 20

In the background, listen on port 2345 and respond with the level 20 password (create server)
```
nc -l 2345 < /etc/bandit_pass/bandit20 & bash
```

Run `setuid` binary on the same port as the server
```
./suconnect 2345
```

Level 21 Password: `secret sbZ2iFcvDpHk8+WSc93s0T5RB2/xt+6EUu4rEuLExanUInK+fCcPU6oujW1egcBqqXNgMXYPEpCThwyFOwt+c0g5gyP+xTfW9dKTgGthCkY=`

#### Level 21

List the contents of the directory `/etc/cron.d`

Print the contents of the relevant cron job

Print the contents of the script that the cron job is running

Print the contents of the file that the script is writing to

Level 22 Password: `secret wYPVbyY8mZlOIKjYK1yQ1FlQ8x7DDzoKaTo4iqjNtaAdCn1UXcsw5AxifxMCYxWvjbH5vr0VlJOSdO8sqD3r69qlT92sxfEtdcKisAnisK0=`

#### Level 22

Same as Level 21 steps

To find folder `$mytarget`, run the code that creates the `mytarget` variable, replacing `$myname` with target user (`bandit23`)

Level 23 Password: `secret dlUuLXs/D+Xz32fSKEWKCzBTjQv3vi5KiJiIZpuNqtW8jaZEFoM0UKejKAPnAM/l2d02p+kpG7omSkEat9y+U7GWaCRcihp3LiyRlb7cMCM=`

#### Level 23

Same as previous 2 levels

Discover script that runs any file owned by user `bandit23`

Create script in a temp directory that copies the `bandit24` password to a temp folder
```bash
#!/bin/bash

mkdir /tmp/tmp.Kd4k4hdkG0

cat /etc/bandit_pass/bandit24 > /tmp/tmp.Kd4k4hdkG0/password24

# improve this by:
# removing password file after a certain amount of time
```

Move this file into the folder that scripts are being executed in

Wait a moment for the cronjob to run and then print the contents of `password24` from the temp folder

Level 24 Password: `secret LPbw5lV4mW+VD/rrQ3hpak+LfPwnRfeBkMCe112JBEfaMARrZ4zCqfUP93JtFmyazwL9b4tJybA8iu4x4yriOJhto/N5ZwsmfqpEUC6PY30=`

#### Level 24

