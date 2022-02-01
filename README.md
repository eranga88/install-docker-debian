# install-docker-debian

# remove default docker packages
sudo apt-get purge docker lxc-docker docker-engine docker.io

# Install Required Packages
sudo apt-get update

sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common

# Install Docker
# Install Docker Using the Repository on Debian 10
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian buster stable"

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io

sudo systemctl status docker

sudo systemctl enable docker
