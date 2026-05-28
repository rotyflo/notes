#### Level 0
Level 1 Password
`secret Sw0P1cP2MiQjflzE2CJifQeXRoFzgNB8Vjsebb4L7SYmZhpE9JBBfM+U5ywLN79NIN5WA41F0rPpKutgKHWNF7sIv2aaDfa09ehv4W2X1jE=`

#### Level 1
`cat ./-`

Level 2 Password
`secret X7Py6xm8k1bXmb42WBpnPcZZYQyQ1VftHSNxuYAcHgmFu3CYxrGvYn2ZY0xjM85MNYgNNg55d3zVpYdB9nzshSrzkhpgaAgbxAsDQhYLev0=`

#### Level 2
Level 3 Password
`secret hvwxpteAavlZWpHxzd9qH4xwig0vVj7JG/wUHTXklV8QjtJObEIboVoubwQP4UldQx1dL/+LUNPseaV5CTkJgBJHdIuLvL2hntTPKdyN3YI=`

#### Level 3
Level 4 Password
`secret iScdUIoLVDTclEBgNCUycEQlmrJIsC/TveAUDHnz+PEweXX58J4hZs0Yo6oGK7498hiHj3vlO0fOPxz0rJEVifdIo1+EqeBGCQGW10Eh7VA=`

#### Level 4
`cat ./*`

Level 5 Password
`secret vdktqr4KvkSYuaFoW4lkBdSyXd8jJFA38JHywmJUi4bkuVds+g7CEjr0ELL+DbS2gFWZPPNPX9Tr92ZI4H+jbz3asZ04RfwIyYZ1NOEIhFM=`

#### Level 5
list recursive, long, all -> find 1033
`ls -Rla | grep 1033`

recursively find `.file2` in current directory and get path of each
`find . -name .file2 -ls`

Level 6 Password
`secret m7GNCtEZy1U8lK37FWGSqULKzSHxm+g6Uscp+Yy06ustT641/ij7+jkyLaAwb3STfsLNIY2hC2WMlRbE+yNc+z/oEGTz8R8Ztp5GmXClpbE=`

#### Level 6
`cd /`
`ls -Rla | grep bandit7`
`find . -name "bandit7.password" -ls`

Level 7 Password
`secret Nu3WFHfeLnQpz55GR2tw9bPik5R1ORP/UcuG26kccFfXeOGgA71aDOctk13bb4aVTvREg6NMVGJWk4m7ivzx/FmqExzXPlwinJH8BaeDhtY=`

#### Level 7
Find the line with the word "millionth"
`cat data.txt | grep millionth`

Level 8 Password
`secret FPeFTGJYCc+xuZtA3hi4YOOpCAkA6L1Q4O1nCsauh1GumtG2uj3v71UEdLU4WD69NayApddRQEgkRujMe2qdbmOhDPhbmt1YYVtrDd8F8MY=`

#### Level 8
Sort data and print the only line that occurs once
`cat data.txt | sort | uniq -u`

Level 9 Password
`secret tgrz/RO/hsDfUhBdZ5SfHz62zuQX2TiX0rajV4JXf8UIoURe6vVHesbtd7SMq0rVvRcfym+eMrdZ8DGE14eNKCa7Ge6dQ1Z1P10yeVKUZdM=`

#### Level 9
Show only human-readable strings and find `===`
`cat data.txt | strings | grep ===`

Level 10 Password
`secret QXyGXSuvQ9qIG6VZJ4SGM8THFY2PfJEFUeFKNnEuU+smhlc4aa5vXa3YLeC17pgvOjO1gELEEFUtHpYzUg5ssUkV1NEjczyrcN9aqJVjnZs=`

#### Level 10
Decode base64
`base64 -d data.txt`

Level 11 Password
`secret 9BGokAFQ+n/eFeNqz0MIEozaGPfmyKLrdCxyGCl6imVsQuuRWQfgWkEzdE1/qKPzqLkA99UWib3cYd0xWweruoi8aa2UEzyYg5cHylBRGaA=`

#### Level 11
rot13 lower
`tr 'a-z' 'n-za-m'`

rot13 UPPER
`tr 'A-Z' 'N-ZA-M'`

rot13 all-case
`tr 'a-zA-Z' 'n-za-mN-ZA-M'`

`cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-M'`

Level 12 Password
`secret 8TCJIezvmSVAQY7i/BkR1W+EDQTSXjMGkRJR79w3SJcTZRl2mCbhMiX+dGPPiFz1AVdUaiem+jixrYLjpMZei1TJPxkavDIFfr3YtIbKq7I=`

#### Level 12
Copy file to new temp directory and work in there
`mktemp -d`

Reverse hexdump
`xxd -r data.txt`

Check file type
`file [filename]`

Rename file to appropriate format and decompress
`gzip -d data.gz`
`bzip2 -d data.bz2`
`tar -xzf data.tar.gz`

Level 13 Password
`secret P68M2YqSieqMfZp1R+KIFMykL3HCvdnLdQT82Y62E9BUFFQQhT+GPxVm2nTrkUZ6ZOfluf9BP7wQsE03D+wSMPZjw9DQEWnm3G+d8m0SqvI=`

#### Level 13
Get the SSH key
`scp -P 2220 bandit13@bandit.labs.overthewire.org:/home/bandit13/sshkey.private .`

Remotely copy file containing password as bandit14 (authenticate with SSH key)
`scp -P 2220 -i sshkey.private bandit14@bandit.labs.overthewire.org:/etc/bandit_pass/bandit14 .`

Fails due to permissiveness. Reduce permissions and copy again.
`chmod 700 sshkey.private`

Level 14 Password
`secret cde9UZ+a3n6UkzQ7TNMXiNMtkqGDUoN3QsP4Ij47jQSymgNmkw47JY0WUPgI4g35ovQudJ8HTvgs8pdmuE2Mrk7w0/klC4VZJG/DCuT/zBs=`

#### Level 14
If you want to see the open ports
`nmap localhost`

`telnet` vs `netcat`
	`netcat` sends/receives raw data on the `transport layer`
	`telnet` establishes interactive session on the `application layer`

Connect to localhost on port 30000 and submit password for this level
`nc localhost 30000`

Level 15 Password
`secret /brVd4pA5UgOeHMo8WQDvusmk58rx1v2ZRqaSzCOKwhnyF56+HxKz9rpHgYJenSLeFtZUNK9pKsW5fQ0uZt7zMTyUTJIm4YQX11bPENwYLI=`

#### Level 15
`ncat` similar to `nc` but with SSL capability

Connect to localhost through port 30001 using SSL/TLS encryption and submit password
`ncat --ssl localhost 30001`

Level 16 Password
`secret 0SvmE24uXA6ju3U0WL5fktTeVH8ioUFG3HQIwf99uB+AG5y0dhrCdCEVKjsBWfl3TddL3ECgn8+KRxa7MDss0A5DPmRcyyguz9mIWZ/lMX4=`

#### Level 16
Run SSL/TLS testing script on ports 31000 to 32000
`nmap --script ssl-enum-ciphers -p 31000-32000 localhost`

Submit password to the SSL encrypted port
`ncat --ssl localhost 31790`

Level 17 SSH Key
`secret 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`

#### Level 17
Save key and use it to authenticate into this level
`ssh -i bandit17.sshkey bandit17@bandit.labs.overthewire.org -p 2220`

