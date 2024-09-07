# Collaborative Development (pico ctf)
## My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

link : https://play.picoctf.org/practice/challenge/410

```bash
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ ls -la
total 32
drwxr-xr-x 3 abhi abhi  4096 Mar 10 02:39 .
drwxr-xr-x 3 abhi abhi 12288 Sep  8 00:19 ..
-rw-r--r-- 1 abhi abhi    30 Mar 10 02:39 flag.py
drwxr-xr-x 8 abhi abhi  4096 Mar 10 02:39 .git
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ cat flag.py
print("Printing the flag...")
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git status
On branch main
nothing to commit, working tree clean
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git log
commit 6ce09adec311b859780caf89d993c58e34b53fa6 (HEAD -> main)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:51 2024 +0000

    init flag printer
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ ls
flag.py
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ cat flag.py 
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$ cat flag.py 
print("Printing the flag...")

print("w0rk_4c24302f}")
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads/drop-in$
```

flag : ```picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_4c24302f}```

# CanYouSee (pico ctf)
## How about some hide and seek?

link : https://play.picoctf.org/practice/challenge/408

```bash
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ ls
ukn_reality.jpg
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ file ukn_reality.jpg 
ukn_reality.jpg: JPEG image data, JFIF standard 1.01, resolution (DPI), density 72x72, segment length 16, baseline, precision 8, 4308x2875, components 3
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ identify ukn_reality.jpg 
Command 'identify' not found, but can be installed with:
sudo apt install graphicsmagick-imagemagick-compat  # version 1.4+really1.3.38-1ubuntu0.1, or
sudo apt install imagemagick-6.q16                  # version 8:6.9.11.60+dfsg-1.3ubuntu0.22.04.5
sudo apt install imagemagick-6.q16hdri              # version 8:6.9.11.60+dfsg-1.3ubuntu0.22.04.5
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ exif
Usage: exif [OPTION...] file
  -v, --version                   Display software version
  -i, --ids                       Show IDs instead of tag names
  -t, --tag=tag                   Select tag
      --ifd=IFD                   Select IFD
  -l, --list-tags                 List all EXIF tags
  -|, --show-mnote                Show contents of tag MakerNote
      --remove                    Remove tag or ifd
  -s, --show-description          Show description of tag
  -e, --extract-thumbnail         Extract thumbnail
  -r, --remove-thumbnail          Remove thumbnail
  -n, --insert-thumbnail=FILE     Insert FILE as thumbnail
      --no-fixup                  Do not fix existing tags in files
  -o, --output=FILE               Write data to FILE
      --set-value=STRING          Value of tag
  -c, --create-exif               Create EXIF data if not existing
  -m, --machine-readable          Output in a machine-readable (tab delimited) format
  -w, --width=WIDTH               Width of output
  -x, --xml-output                Output in a XML format
  -d, --debug                     Show debugging messages

Help options:
  -?, --help                      Show this help message
      --usage                     Display brief usage message
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ exif ukn_reality.jpg 
Corrupt data
The data provided does not follow the specification.
ExifLoader: The data supplied does not seem to contain EXIF data.
abhi@abhi-Lenovo-IdeaPad-S145-15IKB:~/Downloads$ 
```

Image EXIF data:
ExifTool Version Number	12.76
File Name	ezgif-1-dbb4affc9a.jpg
Directory	.
File Size	2.3 MB
File Modification Date/Time	2024:09:07 21:19:42+02:00
File Access Date/Time	2024:09:07 21:19:42+02:00
File Inode Change Date/Time	2024:09:07 21:19:42+02:00
File Permissions	-rw-r--r--
File Type	JPEG
File Type Extension	jpg
MIME Type	image/jpeg
JFIF Version	1.01
Resolution Unit	inches
X Resolution	72
Y Resolution	72
XMP Toolkit	Image::ExifTool 11.88
Attribution URL	cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==
Image Width	4308
Image Height	2875
Encoding Process	Baseline DCT, Huffman coding
Bits Per Sample	8
Color Components	3
Y Cb Cr Sub Sampling	YCbCr4:2:0 (2 2)
Image Size	4308x2875
Megapixels	12.4

suspect : cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==

base64 decoded to : picoCTF{ME74D47A_HIDD3N_4dabddcb}
