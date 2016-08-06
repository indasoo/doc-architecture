# Docker Installation

## Installation on CentOS
https://docs.docker.com/engine/installation/linux/centos/

### Prerequisites
uname -r

### Install with yum
sudo yum update

sudo tee /etc/yum.repos.d/docker.repo <<-'EOF'
[dockerrepo]
name=Docker Repository
baseurl=https://yum.dockerproject.org/repo/main/centos/7/
enabled=1
gpgcheck=1
gpgkey=https://yum.dockerproject.org/gpg
EOF

sudo yum install docker-engine

sudo docker run hello-world

### Install with the script
sudo yum update

curl -fsSL https://get.docker.com/ | sh

sudo service docker start

sudo docker run hello-world

### Create a docker group
sudo groupadd docker
sudo usermod -aG docker docker