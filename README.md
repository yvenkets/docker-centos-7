# Install docker on centos-7

## First remove old versions
sudo yum remove docker docker-client docker-client-latest docker-common docker-latest docker-latest-logrotate docker-logrotate docker-engine

## install

sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

## install specific verion

yum list docker-ce --showduplicates | sort -r

## Syntax
sudo yum install docker-ce-<VERSION_STRING> docker-ce-cli-<VERSION_STRING> containerd.io docker-buildx-plugin docker-compose-plugin

## Example
sudo yum install docker-ce-selinux-17.03.0.ce-1.el7.centos.noarch

## Start docker
sudo systemctl start docker

## test run hello world
sudo docker run hello-world
