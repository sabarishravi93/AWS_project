To accommodate the backup agent tool's specifications, the system admin team at xFusionCorp Industries requires the creation of a user with a non-interactive shell. Here's your task:



Create a user named mark with a non-interactive shell on App Server 1.


Solution :

To create a user named mark with a non-interactive shell on App Server 1, you’ll need to log in to that server and run the appropriate useradd command. A non-interactive shell typically means assigning a shell like /sbin/nologin or /bin/false, which prevents the user from logging in interactively.

Here’s how you can do it:

Log in to App Server 1

bash
ssh tony@<App-Server-1-IP>
(Replace <App-Server-1-IP> with the actual IP from the infrastructure details.)

Create the user with a non-interactive shell

bash
sudo useradd -s /sbin/nologin mark

Verify the user was created with the correct shell

bash
grep mark /etc/passwd
You should see something like:

Code
mark:x:1001:1001::/home/mark:/sbin/nologin