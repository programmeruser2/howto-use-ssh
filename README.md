# How to use SSH
SSH stands for "Secure Shell", and it basically allows you to connect to your computer remotely. Here's a screenshot of `ssh`ing into Ubuntu from a Windows computer:
![ssh](https://storage.googleapis.com/replit/images/1609887960455_4ead522f6be9043ba1ca8369231ec7c6.png)
# Using the SSH Server
First, we need to install the ssh server with:
```bash
sudo apt-get install openssh-server
```
To check that it's running, type:
```
sudo service ssh status
```
(to exit from the command, type 'q')
Make sure to unblock SSH on your firewall. If you're using Ubuntu with `ufw`:
```bash
sudo ufw allow ssh
```
Now that we've setup the server, we need to connect to it with a client.
# Using the SSH Client
Install the SSH client if it isn't already there:
```bash
sudo apt-get install openssh-client
```
Now you can connect to the server:
```bash
ssh <user>@<ip address> -p <port>
```
`<user>` should be replaced with the user you want to login as, `<ip address>` should be the ip address of the computer or the hostname, and `<port>` should be the SSH port. You can find your ip address if you don't know it already with `ip address` (look for `inet`). The `-p <port>` part can be omitted if you set the SSH server to listen on the default port (`22`)
If it asks about the authenticity of the host type `yes`.
Now, it'll ask for your password.
If all goes well then you'll be connected to your remote computer!
Note that if you want to run graphical applications you'll need to have an X server installed.

# Other operating systems
You can find how to install an SSH server on Windows [here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) and how to do it on MacOS [here](https://osxdaily.com/2011/09/30/remote-login-ssh-server-mac-os-x/). You can connect to SSH with the steps [here](https://www.howtogeek.com/311287/how-to-connect-to-an-ssh-server-from-windows-macos-or-linux/).
If you have a chromebook, you can connect to ssh with the steps [here](https://www.howtogeek.com/202768/how-to-use-ssh-tunnelling-on-chrome-os/). You can't start an ssh server without developer mode.

