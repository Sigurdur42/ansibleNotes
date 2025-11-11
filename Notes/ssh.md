Generate private/public on control host
´´´
ssh-keygen -f ~/.ssh/ansible -t ed25519
´´´

Copy the public key to servers:
´´´
ssh-copy-id -i ~/.ssh/ansible.pub <user>@<ip>
´´´

TODO: Lese nach, wie man das Passwort da direkt mit überträgt


### Im Inventory dann noch eintragen
´´´
all:
  vars:
    ansible_ssh_private_key_file: ~/.ssh/ansible
´´´