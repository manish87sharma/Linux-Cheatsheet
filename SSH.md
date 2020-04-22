# SSH basic commands

## login to machine

``` bash
# To login using ssh
> ssh -i <private-key-path> user@ip
> ssh -i <private-key-path> user@hostname
```

## Generate private and public key pair

``` bash
> ssh-keygen
```

## keys command

```bash
# enable agent
> eval $(ssh-agent)
# list keys
> ssh-add -l
# add default key id_rsa
> ssh-add
# add named key
> ssh-add <key-name>
# drop key
> ssh-add -D <key-name>
# add timer
> ssh-add -t seconds <key-name>
```

## directory details

- Default key name **id_rsa**
- SSH directory **.ssh**
- Host details are added to file **known_hosts**
- To restart ssh services on centos

## To restart ssh daemon

```bash
> sudo systemctl start sshd
```  

## Critical ssh files/folders

- ~/.ssh/authorized_keys
- ~/.ssh/config
- ~/.ssh/known_hosts

## SSH config file

- /etc/ssh/ssh_config
- /etc/ssh/sshd_config
  
## permission in ssh folder and files

```bash
# SSH key file permission
> chmod 600 ~/.ssh/id_rsa
# SSH folder permission
> chmod 700 ~/.ssh
> chown -R $USER:$USER ~/.ssh
# Authorized keys file permission
> chmod 644 ~/.ssh/authorized_keys
```

## References

- <https://cheatsheet.dennyzhang.com/cheatsheet-ssh-a4>
- <https://phoenixnap.com/kb/linux-ssh-commands>
- <https://computingforgeeks.com/ssh-cheatsheet-for-sysadmins/>
