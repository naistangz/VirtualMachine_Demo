# Syncing Folders from OS to VM 
 `config.vm.synced_folder "app", "/app"`

The above command will sync OS app to VM


## App folder synced with VM 

## Communication with Devs
- What language is used to build the app
- What framework has been used 
- Are there any dependencies (imported modules) to be installed together 
- What will the app look like 

# Installing Packages

1. Log into your (ve) Server via SSH as the root user
`ssh root@hostname`
`sudo -i`

2. Use apt-get to update your (ve) Server
`root@ubuntu-xenial:~# apt-get update`

3. Installing `nginx`
`root@ubunt-xenial:~# apt-get install nginx`
`service nginx start`

4. Test `nginx`
`sudo nginx -s reload`
**or**
`sudo service nginx reload`
**sudo systemctl status nginx.service**

## Installation
First run as admin 
`$ vagrant@vagrant-ubuntu-trusty-64: ~$sudo -i`

`$ vagrant plugin install vagrant-hostsupdater`

Uninstall with:

`$ vagrant plugin uninstall vagrant-hostsupdater`

Update the plugin with:

`$ vagrant plugin update vagrant-hostsupdater`

## Usage 
```bash
config.vm.network :private_network, ip: '192.168.3.10'
config.vm.hostname = 'www.test.com'
config.hostsupdater.aliases = ["aliases.test"]
```

## Installing dependencies `ruby`
```bash
Anaiss-MacBook-Pro:spec-tests anaistang$ sudo -i
Anaiss-MacBook-Pro:spec-tests anaistang$ gem install bundler
```

## Installing V6 Nodejs
```bash
root@ubuntu-xenial:~# curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
root@ubuntu-xenial:~# npm install pm2 -g
```

## Running tests with Rake
- Rake is a build tool for Ruby
- Rake task runs a set of specs 


![passed_rake](passed_rake.jpeg)

## Chmode `+x`
`chmod +x` on a file (script) makes the file executable file.
`chmod` change mode - modify file access rights 
`chown` change owner - change file ownership
`chgrp` change group owner - change a file's group ownership
Files and directories in Unix may have three types of permissions:
1. read `r`
2. Write `w`
3. Execute `x`

```bash
vagrant@ubuntu-xenial:~$ ls
app
vagrant@ubuntu-xenial:~$ touch nginx_installation_script.sh
vagrant@ubuntu-xenial:~$ ls
app  nginx_installation_script.sh
vagrant@ubuntu-xenial:~$ chmod +x nginx_installation_script.sh
vagrant@ubuntu-xenial:~$ ./nginx_installation_script.sh
```

`top` shows all programs running on the system
`ps` commands gives ProgramID
`chmod +x` file_name.sh
`cat filename` (concatenate) command to display the file content on terminal
 To change directory permissions in Linux, use the following:
- **chmod +rwx filename** to add permissions
- **chmod -rwx directoryname** to remove permissions
- **chmod +x filename** to allow executable permissions
- **chmon -wx filename** to take out write and executable permissions (confidential information)

**Changing directory permissions on Linux for the Group Owners**
- **chmod g+w filename**
- **chmod g-wx filename**
- **chmod o+w filename**
- **chmod o-rwx foldername**

**Changing permissions in numeric code in linux**
0 | No Permission
---|-----
1| Execute
2| Write
4| Read

**Therefore:**
0|---
---|---
1|--x
2|-w-
3|-wx
4|r-
5|r-x
6|rw-
7|rwx

**For example:**

- **chmod 777 foldername** will give read, write, and execute permissions for everyone
- **chmod 700 foldername** will give read, write and execute permissions for the user only
- **chmod 327 foldername** will give write and execute (3) permission for the user, w(2) for the group, and read, write, and execute for the users.

# Provisioning with bash scripts 
```bash
config.vm.provision "shell", path: "environment/provision.sh"
```
First `vagrant destroy`
Then `vagrant up`

`config.vm.provision` - Configures provisioners (refers to process of setting up IT infrastructure) on the machine, so that software can be automatically installed and configured when the machine is created.
`config.vm.synced_folder` - Configures synced folders on the machine, so that folders on your host machine can be synced to and from the guest machine. 
# Launching Node App
# Running tests 



