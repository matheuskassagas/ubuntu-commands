# First step
```
sudo apt-get upgrade -y
sudo apt-get update
```

#Atualizar Snap 
$sudo killall snap-store

$sudo apt update && sudo apt full-upgrade -y && sudo apt autoremove -y && sudo apt autoclean && sudo snap refresh

#Remover drivers da placa de video
$sudo apt-get remove --purge nvidia-* -y

$sudo ubuntu-drivers autoinstall

$sudo reboot

$sudo add-apt-repository ppa:graphics-drivers/ppa && sudo dpkg --add-architecture i386 && sudo apt update && sudo apt install -y nvidia-driver-515 libvulkan1 libvulkan1:i386

# Install DOCKER on ubuntu

$ sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

$ sudo mkdir -p /etc/apt/keyrings

$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

$ echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

$ sudo apt-get update

$ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin

$ sudo docker run hello-world

$ sudo chmod 666 /var/run/docker.sock

$docker login

#Install Kubernets
$sudo apt-get install -y kubectl

$sudo install minikube-linux-amd64 /usr/local/bin/minikube

$curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

#Install PIP on Ubuntu
$ sudo apt-get -y install python3-pip

#Install PYTHON on Ubuntu
$ sudo apt install python3

$pip3 install localstack

$pip3 install awscli-local

$pip3 install terraform-local

localstack start -d
localstack status docker
localstack status services

#Install GIT on Ubuntu
$ sudo apt install git
$ git config --global user.email "<email>"
$ git config --global user.name "<user>"





