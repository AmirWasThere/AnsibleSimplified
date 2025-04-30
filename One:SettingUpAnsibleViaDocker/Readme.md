### Setting up Ansible via Docker
This setup allows you to run Ansible inside a Docker container, making it portable and isolated from your host environment. Prerequisites:
- Docker installed on your local machine
- A Dockerfile for building the Ansible image [located in project directory]

**Project Structure:**
```bash
.
├── Dockerfile          #for building the Ansible image
```

### How to use
**Check the docker installation:**
```bash
docker --version
```
**Build the Docker Image from your Dockerfile**
```bash
docker build -t myansible .
```
**Run the Ansible Container**

To run container from source image `myansible` with name ansible container (-dit: detached, interactive, tty):
```bash
docker run -dit --name ansible-container myansible
```

**Access the Container Shell**
To interact with the container, you can open a shell inside it. 
```bash
docker exec -it ansible-container bash
```
**Verify Ansible Installation**
```bash
ansible --version
```
You should see output with the version of Ansible installed, confirming that everything is set up correctly.
