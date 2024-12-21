# Project-Assignment
Step 1
I created a static IP address 16.171.217.169 and associated it with my EC2 instance

![image](https://github.com/user-attachments/assets/5f396329-b88a-430f-8344-9469b4ce44bf)

I launched/Started my instance  JoyServer

![image](https://github.com/user-attachments/assets/624b25a7-8aa5-4734-8944-e1875614a000)
![image](https://github.com/user-attachments/assets/053513f1-1b2f-404b-bc0d-bb556d415925)


I updated my Server running the command ~sudo apt update~

![image](https://github.com/user-attachments/assets/55d16062-f027-4a5d-926c-3a591d8eebb9)

~sudo apt install apache2~
![image](https://github.com/user-attachments/assets/5e7e1633-4c8c-4b7b-b197-aa1662799d20)
![image](https://github.com/user-attachments/assets/c07ee9c1-78e7-4c26-be6d-855b1cac084f)
![image](https://github.com/user-attachments/assets/9cdd03a9-194e-4718-8594-4a8dc3dde6c4)
![image](https://github.com/user-attachments/assets/82787a34-7fa4-474d-8c5f-70cb5f298b31)

Started and Enabled Apache Server

![image](https://github.com/user-attachments/assets/54f1cb83-e814-4475-923f-a9179b4e9669)

Created an Inbound rule to open HTTP on port 80 and HTTPS on port 443
![image](https://github.com/user-attachments/assets/0ea18da4-01e1-402e-88a5-cd265f852e25)

Now my IP address 16.171.217.169 is accessible on the World Wide Web (www)

![image](https://github.com/user-attachments/assets/0e1c1a78-20a8-4f8c-9535-10d3fc8450e1)

I created an HTML file with a little detail about myself and then deployed the page to my Ubuntu Server
![image](https://github.com/user-attachments/assets/d88fe9d7-ce89-42ba-a317-951f7b3db9af)

Lost permission, I was unable to upload 
* scp: dest open "/var/www/html/index.html": Permission denied
* scp: failed to upload file /Users/HomePC/Documents/index.html to /var/www/html/
![image](https://github.com/user-attachments/assets/368d8495-2e65-4bfb-a1de-d2acc797dd3d)

I needed to allow permissions to the ubuntu user as it only allowed the root user.
I logged on to my server: ssh -i JoyServer.pem ubuntu@16.171.217.169

Ran the commands to check and allow permission: ls -ld /var/www/html/
 
sudo chown -R ubuntu:www-data /var/www/html/
sudo chmod 755 /var/www/html/

![image](https://github.com/user-attachments/assets/f8ace3c2-f535-445c-afaa-b88fe8f3df87)

![image](https://github.com/user-attachments/assets/8cc64e1b-ff32-473e-ba4c-fcd3b7eefc95)


My HTML page on the browser

![image](https://github.com/user-attachments/assets/8d32e315-3e0e-457c-b133-37f8348744f3)



















