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

To start a Kubernetes cluster type following command:

	kubectl create -f pod-definition.yml

![alt text](./images/pod-created.png)

To check all the pods and their health type the following command:

	kubectl get pods

![alt text](./images/get-pod.png)

You can use Dashboard to get an overview of applications running on your cluster, as well as for creating or modifying individual Kubernetes resources (such as Deployments, Jobs, DaemonSets, etc)

The Dashboard UI is not deployed by default. To deploy it, run the following command:

	kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0/aio/deploy/recommended.yaml

You can access Dashboard using the kubectl command-line tool by running the following command:

	kubectl proxy 

![alt text](./images/dashboard.png)

There are two options to authenticate our Kubernetes dashboard account; using either the token or the kubeconfig method. I used the token method given in this [blod](https://www.replex.io/blog/how-to-install-access-and-add-heapster-metrics-to-the-kubernetes-dashboard).

When you access Dashboard on an empty cluster, you'll see the welcome page. This page contains a link to this document as well as a button to deploy your first application. Dashboard lets you create and deploy a containerized application as a Deployment and optional Service with a simple wizard. 

![alt text](./images/WebUI-dashboard.png)

