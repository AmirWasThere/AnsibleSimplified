### Setting up Ansible via Docker
Simply Locate Dockerfile, to build image:
```bash
docker build -t my-ansible .
```
to run docker container from source image "myansible" with name ansible container (-dit: detached, interactive, tty):
```bash
docker run -dit --name ansible-container my-ansible
```
to access container shell: 
```bash
docker exec -it ansible-container bash
```
for testing:
```bash
ansible --version
```
