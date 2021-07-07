# Docker Ansible container

From https://iceburn.medium.com/run-ansible-with-docker-9eb27d75285b

# build

`docker build -t ansible-container:latest .`

# aliases

```sh
alias ansible='docker run -v "${PWD}":/work:ro --rm ansible-container:latest'
alias ansible-playbook='docker run -v "${PWD}":/work:ro -v ~/.ansible/roles:/root/.ansible/roles -v ~/.ssh:/root/.ssh:ro --rm ansible-container:latest ansible-playbook'
alias ansible-vault='docker run -v "${PWD}":/work:ro --rm ansible-container:latest ansible-vault'
```
