
I have created new user called "ambith" and doing operation on that.


ssh-access
Grant/Revoke SSH access to a group of instances to a user.

To add new user and grant SSH access.
ansible-playbook -i inventory/ -e "action=grant" playbooks/ssh.yml

To grant SSH access to an existing user.
ansible-playbook -i inventory/ -e "action=grant" playbooks/ssh.yml --skip-tags=add

To revoke SSH access from a user.
ansible-playbook -i inventory/ -e "action=revoke" playbooks/ssh.yml --skip-tags=remove

To remove user, hence revoke SSH access as well.
ansible-playbook -i inventory/ -e "action=revoke" playbooks/ssh.yml