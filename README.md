# IT-repository
 
Mynewfile

stage 2 deliverables

1 list all top processes running on your system
ps -ef, top or top lsof


2 show system performance matrix


3 list all fundamental linux directories
/
/etc
/cdrom
/dev
/bin
/home
/boot


4 create directories and manipulate the acl
mkdir data1
getfacl data1
groupadd sales
useradd -mG sales jen
id-- im a root user at the moment
chgrp sales data1- changed group ownership for data1 directory, owner remained as root
getfacl data1

groupadd finance 
setfacl -m d:g:finance:rw data1
getfacl data1.... now the group also has rw access to the data1 directory

- adding a user and granting the user access to data1 directory
useradd ben
setacl -m u:ben:rwx data1

5 Migration of object from outside to the server
copying a remote file to local host
scp -r ec2-user@ip-172-31-26-47:sales /home/ec2-user

6 Migration within  the server
ssh-keygen
copied public key
opened new terminal 
ls -la
cd .ssh
vi authorizedkeys
pasted public key from local server
hostname'copy id adress for remote server
back in local server 
ssh ip-172-31-26-47


7 file compression and manipulation
vi planets
- theres a list of planets :Earth, Mars, Venus, Uranus, Neptune
:wq
- gzip planets....compressed planets file


8 File system operation like formatting and mounting
created a volume in aws
attached it
touch  myusb
sudo mount /dev/xvdf myusb
sudo mkfs /dev/xvdf 
 


