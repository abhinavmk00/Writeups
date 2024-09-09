# Bookmarklet (pico ctf)
## Why search for the flag when I can make a bookmarklet to print it for me? Browse here, and find the flag!

link : https://play.picoctf.org/practice/challenge/406

```javascript
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÒËÉ§©í";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
```
```bash
picoCTF{p@g3_turn3r_6bbf8953}
```

# Blame Game (pico ctf)
## Someone's commits seems to be preventing the program from working. Who is it?

link : https://play.picoctf.org/practice/challenge/405

```bash
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ ls -la
total 32
drwxr-xr-x 3 abhi abhi  4096 Mar 10  2024 .
drwxr-xr-x 3 abhi abhi 12288 Sep  9 18:37 ..
drwxr-xr-x 8 abhi abhi  4096 Mar 10  2024 .git
-rw-r--r-- 1 abhi abhi    22 Mar 10  2024 message.py
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ cat message.py 
print("Hello, World!"
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ cd .git/
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in/.git$ ls -la
total 128
drwxr-xr-x   8 abhi abhi  4096 Mar 10  2024 .
drwxr-xr-x   3 abhi abhi  4096 Mar 10  2024 ..
drwxr-xr-x   2 abhi abhi  4096 Mar 10  2024 branches
-rw-r--r--   1 abhi abhi    24 Mar 10  2024 COMMIT_EDITMSG
-rw-r--r--   1 abhi abhi    92 Mar 10  2024 config
-rw-r--r--   1 abhi abhi    73 Mar 10  2024 description
-rw-r--r--   1 abhi abhi    23 Mar 10  2024 HEAD
drwxr-xr-x   2 abhi abhi  4096 Mar 10  2024 hooks
-rw-r--r--   1 abhi abhi   145 Mar 10  2024 index
drwxr-xr-x   2 abhi abhi  4096 Mar 10  2024 info
drwxr-xr-x   3 abhi abhi  4096 Mar 10  2024 logs
drwxr-xr-x 230 abhi abhi 36864 Mar 10  2024 objects
drwxr-xr-x   4 abhi abhi  4096 Mar 10  2024 refs
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in/.git$ cd logs/
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in/.git/logs$ ls
HEAD  refs
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in/.git/logs$ cat HEAD 
0000000000000000000000000000000000000000 f3cec26cf7f80f91b5c3d1972f14dd4e9f97ec83 picoCTF <ops@picoctf.com> 1710018541 +0000	commit (initial): create top secret project
f3cec26cf7f80f91b5c3d1972f14dd4e9f97ec83 9ae3e1bc67ad0143c611c5f65399b79850d20983 picoCTF{@sk_th3_1nt3rn_b64c4705} <ops@picoctf.com> 1710018541 +0000	commit: optimize file size of prod code
9ae3e1bc67ad0143c611c5f65399b79850d20983 ce686edb088333819c3d851f46d0f2e974abdb60 picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
ce686edb088333819c3d851f46d0f2e974abdb60 fc624f29e4524e162adf22e0b16f5b96ab72d59c picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
fc624f29e4524e162adf22e0b16f5b96ab72d59c bf50593cfe791d22959d69cfafabc79baa7c680a picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
bf50593cfe791d22959d69cfafabc79baa7c680a cc1a09bdfa2d00b2c68c49476ca19019c9f9f7d6 picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
cc1a09bdfa2d00b2c68c49476ca19019c9f9f7d6 c659617bfdf75d3f4d56c0342c1f7a58b4cf77da picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
c659617bfdf75d3f4d56c0342c1f7a58b4cf77da 40c8bbcdaa52fee64fa8d9f23d637f3cbfe299ca picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
40c8bbcdaa52fee64fa8d9f23d637f3cbfe299ca 5482dc2d25d36e0acaa6e9635175c89f42f08c04 picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
5482dc2d25d36e0acaa6e9635175c89f42f08c04 9bb77fc42ba458b4ddc8d2fa4f4c87cbe012ec3c picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
9bb77fc42ba458b4ddc8d2fa4f4c87cbe012ec3c 07bf0c44c54316b78a29f1109ad4d7eaeb96d41d picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
07bf0c44c54316b78a29f1109ad4d7eaeb96d41d cae4d5cb5f8a51f09e35d74b5225ce53c62939ad picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
cae4d5cb5f8a51f09e35d74b5225ce53c62939ad 3baadc7dea49213c90831e0894b898d6dabe9a9f picoCTF <ops@picoctf.com> 1710018541 +0000	commit: important business work
...
```

```bash
picoCTF{@sk_th3_1nt3rn_b64c4705}
```

# binhexa (pico ctf)
## How well can you perfom basic binary operations?

link : https://play.picoctf.org/practice/challenge/404

```bash
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in/.git/logs$  nc titan.picoctf.net 62824

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 00011010
Binary Number 2: 00000011


Question 1/6:
Operation 1: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00011101
Correct!

Question 2/6:
Operation 2: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000010
Correct!

Question 3/6:
Operation 3: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10010110
Incorrect. Try again
Enter the binary result: 01001110
Correct!

Question 4/6:
Operation 4: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00000001
Correct!

Question 5/6:
Operation 5: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00011011
Correct!

Question 6/6:
Operation 6: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 00110100
Correct!

Enter the results of the last operation in hexadecimal: 34

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6862762d}
```

# repetitions (pico ctf)
## Can you make sense of this file?

```
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKVVZXcE9VazFXV2toT1dHUllDbUY2UWpSWk1GWlhWa2RHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
```
decoded to 
```
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlVkM0JUVWpOUk1WWkhOWGRYCmF6QjRZMFZXVkdGdGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==
```

decoded to 
```
V1RCa2MyRnRTWGRVYkZaVFltNVNjRmRXYUU5aVJUVnhWVzFhYVdGck5UWmFSVkpQWVRGbmVWVnVR
bHBsYTBweVUxWmpNRTVHWjNsVgpXR1JyVFdwV2VsUlZVbE5oTURCNVZXMWFUd3BTUjNRMVZHNXdX
azB4Y0VWVGFteEVXbm93T1VOblBUMEsK
```

decoded to 
```
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aTwpSR3Q1VG5wWk0xcEVTamxEWnowOUNnPT0K
```

decoded to 
```
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZO
RGt5TnpZM1pESjlDZz09Cg==
```

decoded to 
```
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfNDkyNzY3ZDJ9Cg==
```

decoded to 
```
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_492767d2}
```
