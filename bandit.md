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

Level 17 SSH Key: `secret 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`

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

