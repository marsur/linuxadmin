##### How to protect overwriting /etc/resolv.conf after the reboot? (In network configuration) 

**add PEERDNS="no" to network interface configuration:**

configuration file: https://gitlab.com/martin.suraba/linux_lesson/-/blob/main/network_DNS_issues/ifcfg-ens192_with_PEERDNS.txt


![alt text](https://media.licdn.com/dms/image/D4D12AQFecNrlr4YrOg/article-inline_image-shrink_1500_2232/0/1701177350842?e=1706745600&v=beta&t=lM_8POc8g5LyRXLDBa2tnAGOnB2ssFmP36Vykt6tyJ8))



1) before adding PEERDNS to configuration file will be rewrite via Network Manager



[root@openstackstudy ~]# cat /etc/resolv.conf

<br />
nameserver 8.8.8.8
<br />

2) after adding PEERDNS to configuration file, no rewrite 


[root@openstackstudy ~]# cat /etc/resolv.conf


<br />nameserver 8.8.8.8
<br />nameserver 8.8.4.4


[root@openstackstudy ~]# systemctl restart network

**[root@openstackstudy ~]# cat /etc/resolv.conf**

<br />nameserver 8.8.8.8
<br /> nameserver 8.8.4.4


