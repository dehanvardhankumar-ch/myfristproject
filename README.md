# myfristproject

Install DOCKER in UBUNTU

sudo apt-get remove docker docker-engine docker.io containerd runc

sudo apt-get update


sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release


curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg


echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null


sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io


sudo docker run hello-world




sudo groupadd docker
sudo usermod -aG docker $USER

newgrp docker 

docker run hello-world


 sudo chown "$USER":"$USER" /home/"$USER"/.docker -R

sudo chmod g+rwx "$HOME/.docker" -R




sudo systemctl enable docker.service

sudo systemctl enable containerd.service



SRC URL: https://docs.docker.com/engine/install/ubuntu/


