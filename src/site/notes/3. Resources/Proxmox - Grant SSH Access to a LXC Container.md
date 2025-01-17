---
{"dg-publish":true,"dg-path":"Proxmox - Grant SSH Access to a LXC Container.md","permalink":"/proxmox-grant-ssh-access-to-a-lxc-container/"}
---

****
Use case: When I'm unable to SSH into a [[3. Resources/Proxmox\|proxmox]] container from my machine.

1. **Identify:** First, find the container’s ID or name. Replace {{num}} with the appropriate container identifier in the following commands. 
```
lxc-attach --name {{num}}
```

2. **Edit:** Once inside the container, open the SSH configuration file with a text editor.
```
nano /etc/ssh/sshd_config
```

3. Locate the line PermitRootLogin without-password and update it to:
```
PermitRootLogin yes
```
4. Restart ssh service
```
service ssh restart
```