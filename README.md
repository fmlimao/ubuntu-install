# Instalação do Ubuntu

O código abaixo irá instalar `Git 2`, `NodeJS 10`, `Docker` e `Docker Compose`


## Iniciando com comando root
```bash
sudo su
```

## Programas Básicos
```bash
apt update && \
apt upgrade -y && \
apt dist-upgrade -y && \
apt autoremove -y && \
apt autoclean && \
apt install -y curl vim htop
```

## Git 2
```bash
add-apt-repository ppa:git-core/ppa -y && \
apt update && \
apt install -y git && \
git --version
```

## Chave SSH
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com" && \
eval "$(ssh-agent -s)" && \
ssh-add ~/.ssh/id_rsa && \
cat ~/.ssh/id_rsa.pub
```

## Configuração GIT
```bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## Node 10
```bash
curl -sL https://deb.nodesource.com/setup_10.x | sudo bash - && \
apt install -y python-software-properties nodejs && \
node -v && \
npm -v
```

## Docker
```bash
apt install -y docker.io && \
docker --version && \
docker run hello-world && \
curl -L https://github.com/docker/compose/releases/download/1.23.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose && \
docker-compose --version && \
usermod -aG docker $USER
```
