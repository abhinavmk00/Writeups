# Interencdec (pico ctf)
## Can you get the real meaning from this file.

link : https://play.picoctf.org/practice/challenge/418

```YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgya3lNRFJvYTJvMmZRPT0nCg==```

base64 decoded to 

```b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2kyMDRoa2o2fQ=='```

base64 decoded to 

```wpjvJAM{jhlzhy_k3jy9wa3k_i204hkj6}```

shift cipher brute forced to 

```picoCTF{caesar_d3cr9pt3d_b204adc6}```

# endianness (pico ctf)
## Know of little and big endian?

```bash
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~$ nc titan.picoctf.net 57166
Welcome to the Endian CTF!
You need to find both the little endian and big endian representations of a word.
If you get both correct, you will receive the flag.
Word: ozvjg
Enter the Little Endian representation: gjvzo
Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: ozvg
Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: ozvjg
Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: 103106118122111
Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: 676A767A6F
Correct Little Endian representation!
Enter the Big Endian representation: 6F7A766A67
Correct Big Endian representation!
Congratulations! You found both endian representations correctly!
Your Flag is: picoCTF{3ndi4n_sw4p_su33ess_d58517b6}
```

# Commitment Issues (pico ctf)
## I accidentally wrote the flag down. Good thing I deleted it!

```bash
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ ls -la
total 32
drwxr-xr-x 3 abhi abhi  4096 Mar 12 05:36 .
drwxr-xr-x 3 abhi abhi 12288 Sep  8 00:02 ..
drwxr-xr-x 8 abhi abhi  4096 Mar 12 05:36 .git
-rw-r--r-- 1 abhi abhi    11 Mar 12 05:36 message.txt
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ cat message.txt 
TOP SECRET
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git status
On branch master
nothing to commit, working tree clean
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git log
commit ef0b7cc6b98367fa168573c931e0f7098ef59182 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    remove sensitive info

commit ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    create flag
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git revert HEAD
[master 5ed0e91] Revert "remove sensitive info"
 1 file changed, 1 insertion(+), 1 deletion(-)
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git status
On branch master
nothing to commit, working tree clean
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ cat message.txt
picoCTF{s@n1t1z3_cf09a485}
```