# Getting Started with Kubernetes
Kubernetes is the most important container management technology in the world. This course teaches you the theory and practical skills required to get you up and running as fast as possible.

## Author
[Nigel Poulton](https://app.pluralsight.com/profile/author/nigel-poulton)

## Description
Containers are here and Kubernetes is the de facto platform for running and managing them. In this course, Getting Started with Kubernetes, you'll learn the fundamentals of Kubernetes and the 'Kubernetes way'. First, you'll dive into Kubernetes architecture, what the main components and services are, and how they come together to build a production-class container infrastructure. Next, you'll learn how to get Kubernetes on your laptop as well as a couple of cloud platforms. Finally, you'll deploy an application to Kubernetes using Pods, Services and Deployments. You'll scale the app, test self-healing, perform a rolling update, and finish with a versioned rollback. By the end of this course, you'll have a solid understanding of what Kubernetes is and how it works, as well as skills to deploy a Kubernetes cluster and simple applications.

## Platform
[Pluralsight](https://www.pluralsight.com/)

## Notes

### Instal kubectl
- sudo apt install -y ca-certificates curl gnupg lsb-release apt-transport-https
- sudo curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
- sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

### Install K3d
- curl -s https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash
- k3d cluster create getstartk8s
- k3d cluster start getstartk8s

### Build images
- docker image build -t vsvale/getting-started-k8s:1.0 ./app_v1
- docker image build -t vsvale/getting-started-k8s:2.0 ./app_v2
- docker login
- docker image push vsvale/getting-started-k8s:1.0
- docker image push vsvale/getting-started-k8s:2.0

### apply yamls
- pod: kubectl apply -f ./yamls/pod.yml