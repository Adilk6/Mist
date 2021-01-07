Level 0: used ssh To connect to the server
ssh bandit@bandit.labs.overthewire.org – p 2220
Level 1:
Ls: list of files
Use cat to display content 
First password: boJ9jbbUNNfktd78OOpsqOltutMc3MY1
Level 2:
Ls then cat with  ./ (current directory)
Password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
Level 3: 
simply use cat with backslash so that it gets treated as one file name
Password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
Level 4:
Since it’s hidden use ls then cd inhere/ then when you see the hidden file use cat .hidden
Password: pIwrPrtPN36QITSp3EQaw936yaFoFgAB
level 5:
 use file ./-file* then see all the file data and their types
Password: koReBOKuIDDepwhWk7jZC0RTdopnAYKh
level 6
Use find ./ -size 1033c
Then use cat to get the password
Password: DXjZPULLxYr17uwoI01bNLQbtFemEgo7
Level 7
Use cat data.txt | grep -i millionth
Password: cvX2JJa4CFALtqS87jk27qwqGhBM9plV
Level 8 (to 9):
Use sort along with uniq-c
Password: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
Level 9
Use ls
Then use strings data.txt along with grep searching for “=”
Password: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
Level 10
Use the base64 function i.e. Base64 -d data.txt
Password: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
Level 11
Like the hint said use rot13 cause every letter is rotated by 13 places go to rot13.com
Or Use cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'
Password: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
Level 12
As said create a temporary folder
$ mkdr -v /tmp/brad123
Then reverse the hex dump $ xxd -r data.txt /tmp/brad123/data.txt
Then change directory $ cd /tmp/brad123
/tmp/brad123 ls
Find out the file type
/tmp/brad123 file data.txt
The file is compressed t uncompress it,
Use zcat data.txt > new, you will find a bzip 2 file type after few commands
Use /tmp/brad123 $bzip -dnew


Level 13
You get a ssh key 
$ ssh -i sshkey.private bandit14@localhost
Answer yes, check for pass when in bandit 14 use cat
Password:4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e.
Level 14
Use nc command
$ nc localhost 30000
Then submit password of level 13
Password: BfMYroe26WYalil77FoDi9qh59eK5xNr

Level 15
Use ssl command cause it’s using ssl encryption
Openssl s_client -connect localhost 300001
Then submit the password for level 15
When you get heartbeat use the line given on the website, then submit the password
Password: cluFn7wTiGryunymYOu4RcffSxQluehd.
Level 16

Level 17
the two files in the home directory have ASCII text, use cat and diff to compare the two files
diff password.new…., you get the password corresponding to the password. New
Password: kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd 
Level 18
ssh bandit18@bandit.labs.overthewire.org – p 2220 cat readme because we knew the file was in home directory in cat readme
Password: IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
Level 19
It asks us to run a command as another user, so ./bandit20-do ls /etc/bandit_pass to see the file, you will see bandit 20 file use the same function again so ./bandit20-do ls /etc/bandit_pass/bandit20
Password: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
Level 20

Level 21
