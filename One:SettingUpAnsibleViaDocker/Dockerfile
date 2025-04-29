#sourceImage
FROM python:3.10-slim

RUN pip install --no-cache-dir ansible

WORKDIR /ansible

CMD ["ansible-playbook", "--version"]
