# Advanced-Bash--Owning-the-System
Homework 6

Step 1: Shadow People

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

Test that sudo access works without your password: Your bash commands here

sudo sysd
sudo cat /etc/shadow

![image](https://github.com/user-attachments/assets/962bb097-cb3b-43dd-8e1b-d9b6519c2a1c)


Step 2: Smooth Sailing
Edit the sshd_config file: sudo nano sshd_config Your bash commands here

Port 22 Port 2222

![image](https://github.com/user-attachments/assets/5e55f1f6-affc-479f-b346-ee62d120e9d3)


Step 3: Testing Your Configuration Update

Restart the SSH service: Your solution command here

service ssh restart

![image](https://github.com/user-attachments/assets/a9547001-4fc9-4876-b2c8-94763efed92c)


SSH to the target machine using your sysd account and port 2222: Your solution command here

ssh sysd@192.168.6.105 -p 2222

