# Passwordless Authentication

### 1. Using SSH Key:

```
ssh-copy-id -f "-o IdentityFile <PATH TO PEM FILE>" user@<INSTANCE-PUBLIC-IP>
```
- `ssh-copy-id`: This commmand copies my(local machines) public key in the remote instance authorized_key file (~/.ssh/authorized_keys). In this case its `INSTANCE-PUBLIC-IP` instance. 
-  `f`: This flag forces the installation/copying of the key even if the key is already present/installed on the remote instance.
-  `o IdentityFile` is used to pass options to the SSH client or pointing to the .pem file. Its identity file, which is private key (.pem file) of `INSTANCE-PUBLIC-IP` for authentication and -o 

### 2. Using user and password:

- Go to file `/etc/ssh/sshd_config`
- Edit `PasswordAuthentication yes`
- Add password using to the user using command `sudo passwd username`
- Restart SSH service `sudo systemctl restart sshd.service`
- `ssh-copy-id user@<INSTANCE-PUBLIC-IP>`

