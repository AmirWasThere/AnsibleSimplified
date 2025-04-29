### Setting up Ansible via Docker
Simply Locate Dockerfile, then:
```bash
docker run -it --rm -v $(pwd):/ansible -w /ansible my-ansible
```
docker run: Launches a new Docker container

-it: Interactive with TTY

-v $(pwd):/ansible: Mounts your current directory into the container at /ansible. This allows the container to access your playbook files.

-w /ansible: Sets the working directory inside the container to /ansible

my-ansible: The name of the Docker image that has Ansible installed
