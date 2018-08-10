# Instalação do Ubuntu

```bash
sudo apt-get update -y && \
sudo apt-get upgrade -y && \
sudo apt-get dist-upgrade -y && \
sudo apt-get autoremove -y && \
sudo add-apt-repository ppa:git-core/ppa -y && \
sudo apt-get update && \
sudo apt-get install git -y && \
git --version && \
sudo apt-get install -y curl vim htop && \
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash - && \
sudo apt-get install -y nodejs build-essential npm && \
node --version && \
npm --version && \
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
sudo groupadd docker && \
sudo usermod -aG docker $USER && \
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 931FF8E79F0876134EDDBDCCA87FF9DF48BF1C90 && \
echo deb http://repository.spotify.com stable non-free | sudo tee /etc/apt/sources.list.d/spotify.list && \
sudo apt-get update && \
sudo apt-get install -y spotify-client && \
sudo apt-get install -y mysql-workbench && \
sudo apt-get install -y mysql-server && \
sudo apt-get install -y php7.2 php7.2-cli php7.2-fpm php7.2-xml php7.2-common php7.2-curl php7.2-mysql php7.2-zip

```

vscode
gitkraken
stride
slack
skype