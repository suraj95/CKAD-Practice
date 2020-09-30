# CKAD-Practice

![alt text](./images/ckad-logo.png)

The [Certified Kubernetes Application Developer (CKAD)](https://www.cncf.io/certification/ckad/) program has been developed by the Cloud Native Computing Foundation (CNCF), in collaboration with The Linux Foundation, to help expand the Kubernetes ecosystem through standardized training and certification. Certification is a key step in that process, allowing certified application developers to quickly establish their credibility and value in the job market, and also allowing companies to more quickly hire high-quality teams to support their growth.

The online, proctored, performance-based test consists of a set of performance-based items (problems) to be solved in a command line and is expected to take approximately two (2) hours to complete.

This exam curriculum includes these general domains and their weights on the exam:

* 13% – Core Concepts
* 18% – Configuration
* 10% – Multi-Container Pods
* 18% – Observability
* 20% – Pod Design
* 13% – Services & Networking
* 8% – State Persistence

# Working with Kubernetes

Kubernetes (K8s) is an open-source system for automating deployment, scaling, and management of containerized applications. It groups containers that make up an application into logical units for easy management and discovery. 

The following command runs kubectl in a mode where it acts as a reverse proxy. 

	kubectl proxy --port=8080 &

Creates a proxy server or application-level gateway between localhost and the Kubernetes API Server. It also allows serving static content over specified HTTP path. All incoming data enters through one port and gets forwarded to the remote kubernetes API Server port, except for the path matching the static content path. Then you can explore the API with curl, wget, or a browser, like so:

	curl http://localhost:8080/api/ 	

Minikube is an open source tool that enables you to run Kubernetes on your laptop or other local machine. It can work with Linux, Mac, and Windows operating systems. It runs a single-node cluster inside a virtual machine on your local machine.

The easiest way to install Minikube on macOS is using Homebrew:

	brew install minikube

Start Minikube and create a cluster:

	minikube start

![alt text](./images/minikube.png)

Once minikube start finishes, run the command below to check the status of the cluster:

	minikube status

![alt text](./images/minikube-status.png)

To start a Kubernetes cluster type following command

	kubectl create -f pod-definition.yml




