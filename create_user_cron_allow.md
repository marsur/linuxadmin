
**How to create user and allow to cron?**


[root@openstackstudy ~]# useradd user3
<br/>
[root@openstackstudy ~]# passwd user3
<br/>
Changing password for user user3.
<br/>
New password:
<br/>
BAD PASSWORD: The password is shorter than 8 characters
<br/>
Retype new password:
<br/>
passwd: all authentication tokens updated successfully.
<br/>
<br/>
[root@openstackstudy ~]# vi /etc/cron.allow
<br/>
[root@openstackstudy ~]# su user3
<br/>
[user3@openstackstudy root]$ crontab -e
<br/>
no crontab for user3 - using an empty one
<br/>
crontab: no changes made to crontab
<br/>
