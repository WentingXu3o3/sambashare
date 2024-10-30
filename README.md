# sambashare
how to enable sambashare on ubuntu system


# on ubuntu
##1.sudo apt update && sudo apt isntall samba

##2.sudo chown username:username ~/shared_folder
    sudo chmod 777 ~/shared_folder

##3.sudo nano /etc/samba/smb.conf

##4.add these at the bottom of the conf file
```
[YourSharedFolderName]
path = /home/xxx/shared_folder
browseable = yes
read only = no
valid users = yourusername
guest ok = no
```

##5.sudo systemctl restart smbd

# on your mac
##1.at finder, go connect to server

##2.smb://yourhostip/ connect

##3.done
