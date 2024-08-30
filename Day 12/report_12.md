# SQLi (medium)
## Assigment 12

### In this case there is a option to avoid user input
![](./pics/1.png)
### Viewing the code
![](./pics/2.png)
### Starting burp suit to intrsept the http request
![](./pics/3.png)
### Turning on the intersept and sending the request
![](./pics/4.png)
### Examining the intersepted packet
![](./pics/5.png)
### Adding the sql injection into it `UNION SELECT user, password FROM users --` id feild
![](./pics/6.png)
### Forwarding the packet and receving the hashed password
![](./pics/7.png)