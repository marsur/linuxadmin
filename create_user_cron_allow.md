
**How to create user and allow to cron?**


[root@openstackstudy ~]# useradd user3
[root@openstackstudy ~]# passwd user3
Changing password for user user3.
New password:
BAD PASSWORD: The password is shorter than 8 characters
Retype new password:
passwd: all authentication tokens updated successfully.


[root@openstackstudy ~]# vi /etc/cron.allow
[root@openstackstudy ~]# su user3

[user3@openstackstudy root]$ crontab -e
no crontab for user3 - using an empty one
crontab: no changes made to crontab
