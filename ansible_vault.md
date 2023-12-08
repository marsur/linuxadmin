**How to create ansible-vault to playbook? **


 new file
ansible-vault create crontab.yaml

#you don't see the content 
cat crontab.yaml 

#how to decrpyt
ansible-vault decrypt crontab.yaml 

#you see  the content 

cat crontab.yaml 

#encrypt file which exists 

ansible-vault encrypt crontab.yaml

# how to start playbook with asking password 

ansible-playbook crontab.yaml --ask-vault-pass


ansible-vault create example.yml: create an encrypted file
ansible-vault edit example.yml: edit an encrypted file
ansible-vault view example.yml: view an encrypted file
ansible-vault rekey example.yml: change the password of an encrypted file
ansible-vault encrypt example.yml: encrypt an existing file
ansible-vault decrypt example.yml: decrypt an encrypted file
ansible-vault encrypt_string 'secret': encrypt a variable
ansible-playbook --ask-vault-pass playbook.yml: provide the password to run a playbook with encrypted files
