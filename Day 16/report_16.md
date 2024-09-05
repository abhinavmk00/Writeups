# Binary Search (pico ctf)
## Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses. Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!

link : https://play.picoctf.org/practice/challenge/442

```bash
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500 
Higher! Try again.
Enter your guess: 800
Lower! Try again.
Enter your guess: 650
Lower! Try again.
Enter your guess: 575
Higher! Try again.
Enter your guess: 625
Higher! Try again.
Enter your guess: 640
Lower! Try again.
Enter your guess: 633
Lower! Try again.
Enter your guess: 629
Congratulations! You guessed the correct number: 629
Here's your flag: picoCTF{g00d_gu355_1597707f}
``` 
# format string 0 (pico ctf)
## Can you use your knowledge of format strings to make the customers happy?

link : https://play.picoctf.org/practice/challenge/433

```bash
Welcome to our newly-opened burger place Pico 'n Patty! Can you help the picky customers find their favorite burger?
Here comes the first customer Patrick who wants a giant bite.
Please choose from the following burgers: Breakf@st_Burger, Gr%114d_Cheese, Bac0n_D3luxe
Enter your recommendation: Gr%114d_Cheese
Gr                                                                                                           4202954_Cheese
Good job! Patrick is happy! Now can you serve the second customer?
Sponge Bob wants something outrageous that would break the shop (better be served quick before the shop owner kicks you out!)
Please choose from the following burgers: Pe%to_Portobello, $outhwest_Burger, Cla%sic_Che%s%steak
Enter your recommendation: Cla%sic_Che%s%steak
ClaCla%sic_Che%s%steakic_Che(null)
```

# Super SSH (pico ctf)
## Using a Secure Shell (SSH) is going to be pretty important.Can you ssh as ctf-player to titan.picoctf.net at port 60608 to get the flag? You'll also need the password 84b12bae. If asked, accept the fingerprint with yes.

```bash
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~$ ssh -p 60608 ctf-player@titan.picoctf.net
The authenticity of host '[titan.picoctf.net]:60608 ([3.139.174.234]:60608)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:60608' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_07a987ac}
Connection to titan.picoctf.net closed.
```
