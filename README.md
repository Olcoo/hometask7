Hometask_7


First step: creating new ssh key and set it on

STEPS:
ssh-keygen -t rsa - add new keys(and write the path)

ssh-add /home/devops-pc/.ssh/id_rsa - connect your private key to your machine

ssh-copy-id -i /home/devops-pc/.ssh/id_rsa.pub -p4022 root@yoko.ukrtux.com - used to add an ssh key to a remote machine

ssh -p4022 root@yoko.ukrtux.com - check your connect(should not ask for a password)

ssh - D8888 -p4022 root@yoko.ukrtux.com - enter through the port we opened

Second step: pushing our server and take reverse connect to your server through the firewall.

STEPS:
python3 -m http.server 8866 - use this command while in the directory with the project you want to push.

ssh -R 14022:localhost:8866 -p4022 root@yoko.ukrtux.com - create reverse connect to your server.

