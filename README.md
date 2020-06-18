# Install-Kubernetes-Ubuntu
##  Project Overview

The purpose of this project was to install K8S on Ubuntu VM by Setting up a Kubernetes cluster and learn the basics of K8S commands by applying it to my docker image [website hosted on Nginx container](https://hub.docker.com/repository/registry-1.docker.io/samir2296/containerization/tags?page=1).

### What are the benefits of using K8S?
K8S is container orchestrator used to automate, configure and scheduling of containers at differnet node. K8s helps that big monolithic legacy applications are being broken down into smaller, independently running components called microservices. 
K8S enables you to change components quickly and as often as necessary to keep up with today’s rapidly changing business requirements.

## Steps to install Kubernetes on Ubuntu:
1- Disable swap memory on both the nodes by running the following command:
 ```
 sudo swapoff -a
 ```

2- Install the Docker utility on both the nodes by running the following command :
 ```
sudo apt install docker.io.

 ```
3-  sudo systemctl enable docker.

4- sudo apt install curl.

5- curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add.

6- sudo apt-add-repository "deb http://apt.kubernetes.io/ kubernetes-xenial main".

7- sudo apt install kubeadm.

8- sudo kubeadm init --pod-network-cidr=10.244.0.0/16.(on master node only)

9- sudo kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml. (Deploy a Pod Network on master node).


