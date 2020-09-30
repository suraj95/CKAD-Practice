# CKAD-Practice


The following command runs kubectl in a mode where it acts as a reverse proxy. It handles locating the API server and authenticating.

Run it like this:

	kubectl proxy --port=8080 &

	curl http://localhost:8080/api/ 	

Minikube is an open source tool that enables you to run Kubernetes on your laptop or other local machine. It can work with Linux, Mac, and Windows operating systems. It runs a single-node cluster inside a virtual machine on your local machine.

The easiest way to install Minikube on macOS is using Homebrew:

	brew install minikube

	minikube start

![alt text](./images/minikube.png)

To start a Kuberntes cluster type following command

	kubectl create -f pod-definition.yml




