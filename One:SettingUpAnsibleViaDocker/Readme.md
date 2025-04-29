### Setting up Ansible via Docker
Simply Locate Dockerfile, to build image:
```bash
docker build -t my-ansible .
```
To run docker container from source image "myansible" with name ansible container (-dit: detached, interactive, tty):
```bash
docker run -dit --name ansible-container my-ansible
```
To access container shell: 
```bash
docker exec -it ansible-container bash
```
For testing:
```bash
ansible --version
```
