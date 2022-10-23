# Getting-Started-with-Kubernetes

## Instal kubectl
- sudo apt install -y ca-certificates curl gnupg lsb-release apt-transport-https
- sudo curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
- sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

## Install K3d
- curl -s https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash
- k3d cluster create getstartk8s
- k3d cluster start getstartk8s

## Build image
- docker image build -t vsvale/getting-started-k8s:1.0 ./app
- docker login
- docker image push vsvale/getting-started-k8s:1.0