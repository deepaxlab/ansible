# Passwordless Authentication

### using SSH Key:

```
ssh-copy-id -f "-o IdentityFile <PATH TO PEM FILE>" ubuntu@<INSTANCE-PUBLIC-IP>
```


### using user and password:

- Go to file `/etc/ssh/sshd_config`
- Edit `PasswordAuthentication yes`
- Restart SSH service `sudo restart sshd.service`

