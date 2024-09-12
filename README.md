# Advanced-Bash--Owning-the-System
Homework 6

Create a secret user named sysd. Make sure this user doesn't have a home folder created: Your solution command here

sudo adduser sysd

![image](https://github.com/user-attachments/assets/4ce727e9-e075-41a7-889d-845fee52295d)


Give your secret user a password: Your solution command here

sudo passwd sysd

![image](https://github.com/user-attachments/assets/c8484ac9-f552-4a31-943d-394f14889441)


Give your secret user a system UID < 1000: Your solution command here

sudo usermod -u 160 sysd
Give your secret user the same GID: Your solution command here

sudo groupmod -g 100 sysd

![image](https://github.com/user-attachments/assets/c81edddb-84a0-4721-92e6-6f8201d643fc)


Give your secret user full sudo access without the need for a password: Your solution command here

sudo visudo

![image](https://github.com/user-attachments/assets/0c2a0553-2e1e-43b6-a04d-71cd45d55edf)


