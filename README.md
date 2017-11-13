# Instalação do Ubuntu

O código abaixo irá instalar: Git 2, NodeJS 6, Docker, Docker Compose e o Laradock na versão 5.5

```bash
sudo add-apt-repository ppa:git-core/ppa -y && \
sudo apt-get update && \
sudo apt-get install git -y && \
git --version && \
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash - && \
sudo apt-get install nodejs -y && \
sudo apt-get install build-essential -y && \
node --version && \
sudo apt-get update && \
sudo apt-get install -y \
    linux-image-extra-$(uname -r) \
    linux-image-extra-virtual && \
sudo apt-get update && \
sudo apt-get install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && \
sudo add-apt-repository -y \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable" && \
sudo apt-get update && \
sudo apt-get install docker-ce -y && \
sudo docker --version && \
sudo docker run hello-world && \
sudo curl -L https://github.com/docker/compose/releases/download/1.16.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose && \
sudo chmod +x /usr/local/bin/docker-compose && \
sudo docker-compose --version && \
mkdir -p ~/Documents/projects && \
cd ~/Documents/projects && \
rm -rf laradock && \
git clone https://github.com/Laradock/laradock.git && \
cd laradock && \
git checkout tags/v5.5.0 && \
git status && \
cp env-example .env
```

Agora precisamos edicar o arquivo `.env` e selecionar a versão do PHP.

Depois podemos executar o `docker-compose`

```
sudo docker-compose up -d nginx mysql mongo
```
