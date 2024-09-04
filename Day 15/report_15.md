# Verify (pico ctf)
## People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate.

link : https://play.picoctf.org/practice/challenge/450

### list the files
```bash
ctf-player@pico-chall$ ls
checksum.txt  decrypt.sh  files
```
### list the files in files/
```bash
ctf-player@pico-chall$ ls files/
0SgkM1fC  7zsihLxd  ETctMG1o  MYdMdURn	Tx4sSuiN  bZEwUIec  mDzgzkrP  sGOAdKy2
0aer7B0J  8N3DHyAn  EYaK1nX6  MavUz60O	UCbhwrDb  blsMKCvn  mMNEp8Zi  sKOkwRCd
0b3lt0HK  8NfqFqEn  FYfLvi5w  Md3PHwRz	UgDsmf5L  bnahMLHf  mg4g9Eoi  svPh5fI5
0ia8IBYb  8OpGe3TY  FcWqkSIP  MvDDPtoW	V3xeKcD7  cO1o2qFY  mqsieQoa  t4IiokLf
0uUAy06x  8WA32dcd  FhDH2g8j  NAwNCfiS	VBHAXd7G  cVywfT1b  myF2mI2w  tenQzijC
17iH5ioj  8WYKhs9b  FkO80Me6  NB0dzXJg	VM5DLaA2  cZXSF7wu  n1PE7llz  tkv0UoX3
1CY2Hque  8d6678sz  FlEOSTL0  NHSLSull	VU1Tnx8J  cdZ1Ao5D  n6yqXRv8  tmkJMhbV
1LPOMJE7  9LMKbufv  GEtA0Z9a  NYT2nPuv	VZqopSEM  chvVzQdY  nSepPhk6  ud4LEsxA
1P5dsfLj  9YFDyvy5  GFWqPjn6  NlN25jkt	Vc1VEpYz  cmhkISVH  nTEqj1Ol  uhLtbHVL
1Tst6fbt  9rtRtn1R  GhwoHV4M  NlymPzCl	Vc6sosw2  cvnPhBaQ  nU797aVT  vQmN5k6y
2CyEUmhf  9wXkj9wB  Gpbebiyr  NrbmwP3r	VhrXhFPH  d0OYmJbG  nVO17uZV  vQtPAQBH
2MgqiK3F  9wzwojIO  H6Mlhvd5  O3c1wd4r	W7K36eZ0  d0rJvLyw  npy5LylP  vmLoCSN5
2R1dcXMM  A2SZHgJV  HS8wBLPJ  OkXybbh3	WYlISi4n  d1usLAwO  nxx3UCp8  vt86VpBP
2SLEujSI  A8X4q2Hn  IMoTEVt4  OtnjktH8	WaA6y2oF  dxJZggkO  oLZldZsM  vzBdlMd6
2cdcb2de  ABh1G8a0  IjkDI0gL  PNNRiq3F	WjUfazgU  eRcEh616  oNfmBvds  w2pqQhei
2eijwTPh  AUijzvDq  IwVJbP5E  PkxFO6fj	WnH4XGQ0  eoW9IJAR  oWfAJ9wj  w80nVzZO
3FOFUCD5  AWnJiVoE  J7BJ7tAo  PoAr7OrB	WnOWGw9n  fpXvjTBY  ocTCyt2G  w8E8Jd9J
3aMAegi2  AfnUEE9s  JD0ZwfH8  PtRzswzh	WwobUdQA  fw6XlbF3  ocoustRi  wHR2ydKC
3laJICck  AgQhab96  JIPRVMlG  QBtXtwy6	WzxM1rI6  g1qINnts  orQXAz13  wvNy3kRU
3mHrLQG2  AlhLQIGI  JLE4rtY5  QCHOeksH	X3z7ayAf  gewOpz6a  oxeNN5uA  xZDQnhCn
3nroY5Wt  Au8Ov7jr  JLuwL5UE  QOHEW95s	X5Vhdb8H  gr99Nl0G  oyrMYyZY  y2XXKk9C
4BRDZhS7  B8RXEf4S  JVT3ckAg  QTetbcxE	Y4FnPPHX  gru5fnYQ  p0qmvEGQ  y8THzTYH
4EqhTV10  BMlbLM49  JhHZxLSp  QcXjRtBd	YEOowfPv  hRF2XNzg  p3lVedu9  yOmzIQym
4Fegg7AZ  BpkwKiOq  JrbVOugk  Qm0B85oQ	YZc8J6Vf  iKH9t6m9  pREkecwB  yTiWOwXD
4gMs4KnO  C0PnAa7J  KAS20Z1p  Qxx5KB3R	YjEaz92U  ih4q9ziU  pV3BIyJh  yb3Ro4yS
4l9DWh5d  C3l9qdYz  KCoDTFB7  R84tLxGR	YkYjwuGz  jQXi84ic  pVFybOWo  ypzAaM0c
5HAN1XjT  CChBmQFs  Ka9uxW6u  RKOBoCMd	ZEEtJ79A  jnOnhjk8  qAUGa8Jx  yzW64294
5ntikrlo  CDg6fdfa  Kc5sfOun  RSQ5Ynin	ZK4affS3  kDlGNWXG  qIqcOTDP  z1DTGQLy
5ymaOO07  CTTDdMGJ  KhnreD4t  RV6BgBu6	ZO3IvMwL  kQMlzWUP  qKIr0SCL  z5y1jgty
6GzNwIbL  CXVq5spu  L9tRKUkW  RWol5Yvg	ZQ7ftng7  kTDaKoIe  qMqcX95Y  zHpAJtSR
6dZQoo4O  Cwfv60OS  LZgQIZ9b  RXQH6a3z	ZZzeAnnA  kvSPifOB  qfWh95Q9  zJHj9Wev
6mT8PiGl  DGOlVleK  LnKLtxdL  RrQhgxZJ	aDI9kNj8  kvpk6rIp  rPOS47wB  zQZjRCvK
760ZV0rr  DINN9cgG  LoSmsO5t  Rrq6u3VG	aUzSODcp  l70cIeRx  rXWuGW1m  zmrLJtwD
7KoII9M8  DNwq8kf8  MAd4OQmU  STlIDlxJ	agmwERM5  l8tB6vEL  rgZiIAPZ  zoSxd2Nl
7NBIv8bi  Dq8qjJ8S  MBaThKzn  Scml7yYd	b5TZpaRr  lEjMl22a  rjta4881  zp4ssY0Q
7Snixk9W  Dr3JaQz7  MLDxW9mt  Sn9XVrp6	b8hbdeFv  lMIM4IQe  ryxNv3Er
7eaPaid5  Dt7YKSAq  MV2AJR5r  TWbymLFA	bMcbuEVi  lbsGcfLr  rzQKjmcB
7ylewstJ  E1grB9Sb  MXItXLsj  TXecNl9L	bVoP3eel  lbszmcDf  s3TrU3bC
```
### Trying to decrypt all the files and failing
```bash
ctf-player@pico-chall$ ./decrypt.sh files/*
bad magic number
Error: Failed to decrypt 'files/0SgkM1fC'. This flag is fake! Keep looking!
```
### finding the file with matching cheacksum as in checksum.txt
```bash
ctf-player@pico-chall$ sha256sum files/*|grep "55b983afdd9d10718f1db3983459efc5cc3f5a66841e2651041e25dec3efd46a"
55b983afdd9d10718f1db3983459efc5cc3f5a66841e2651041e25dec3efd46a  files/2cdcb2de
```
### decrypting the file to get the flag
```bash
ctf-player@pico-chall$ ./decrypt.sh files/2cdcb2de
picoCTF{trust_but_verify_2cdcb2de}
```