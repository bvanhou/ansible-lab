###### Set up Environment
[ ] Verify Environment
    - If you are unable to list all hosts from ansible then install ansible


###### Set up Ansible Tower

```
ansible localhost -m unarchive -a "src=https://releases.ansible.com/ansible-tower/setup/ansible-tower-setup-latest.tar.gz dest=/root/ remote_src=yes"
```

- Create a new file /root/ansible-tower-setup-/inventory to specify list of hosts where Ansible Tower packages shall be deployed and add the hostname for external Postgres database will be deployed and configured. 
    note: You also need to specify the password for Ansible Tower *admin user, postgres user and rabbitmq user.
- Then execute setup.sh to install Ansible Tower and external database server
```
/root/ansible-tower-setup-*/setup.sh
```

