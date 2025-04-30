### Setting up Docker via Ansible
This project uses Ansible to install and configure Docker on one or more Linux hosts. 
What actually do we need?
- Ansible installed on your control machine (e.g. your local system)

- SSH access to the target host(s)

- A user with sudo privileges on the target machine(s)

Project Structure:
```bash
.
├── inventory.ini       #Used to store the addresses and details of targets on which actions are to be performed
├── playbook.yml        #Defines the set of tasks and roles to be executed on target hosts
```
### How to use
Edit the inventory file: Add your target host(s) to `inventory.ini`, for example:
```bash
[dockerhosts]
192.168.1.10 ansible_user=root
```
Ping the target(s):
```bash
ansible dockerhosts -m ping
```
Run the Ansible Playbook:
```bash
ansible-playbook -i inventory.ini playbook.yaml
```
Verify Docker Installation:
```bash
docker --version
```

