# User Permissions
![image](https://user-images.githubusercontent.com/82356945/216409977-2cc67aaa-0244-4404-a394-5070af169160.png)
![](https://pamirwebhost.com/wp-content/uploads/2018/07/Files-permissions-and-ownership-basics-in-Linux.png)

## User Commands
* `sudo adduser [user]` | create a new user
* `su [user]` | switch to user

## Password File
* `cat /etc/passwd` | view other users and services
* `sudo cat /etc/shadow` | view password hashes

## Sudoers
* `sudo cat /etc/sudoers` | view sudoers file
* `sudo cat /etc/group | grep sudo` | view users in the sudo group
