# Prereqs

* Ansible 2.9+
* Cisco ASA 55XX and up
* ASA 9.1+ image
* netcommon module - included in Ansible 2.9 but might be buggy
* asa module - included in Ansible 2.9 but might be buggy

Instead we use the latest version from Ansible Galaxy which is maintained by the offical authors
### Run manually: 
```console
ansible-galaxy collection install cisco.asa
ansible-galaxy collection install ansible.netcommon
```


### Usage example
To add an object:
```console
ansible-playbook playbook.yaml -i inventory.ini --extra-vars "ASA_HOST=10.10.10.1 ASA_USER=cisco ASA_PASS=cisco ASA_ENABLE_PASS=cisco STATE=add ansible_hostname=testname ip=10.10.10.2"
```

To delete an object:
```console
ansible-playbook playbook.yaml -i inventory.ini --extra-vars "ASA_HOST=10.10.10.1 ASA_USER=cisco ASA_PASS=cisco ASA_ENABLE_PASS=cisco STATE=delete ansible_hostname=testname ip=10.10.10.2"
```
