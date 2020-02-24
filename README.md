# Testcroesslend

Cross lend DevOps assignment

#Task 1 Repository
I have created a repository in GitHub where i have uploaded all the neccesary files.
sukhdevVyas/crosslendDevOps

#Task 2 Cluster Configuration

I have created cluster in standalone system using minikube. 

congif.json

Installed two services :

#nginx ingress server
$ cd /nginx-ingress

Create a namespace and a service account for the Ingress controller:

$ kubectl apply -f common/ns-and-sa.yaml

Create a cluster role and cluster role binding for the service account:

$ kubectl apply -f rbac/rbac.yaml

Create a secret with a TLS certificate and a key for the default server in NGINX:

$ kubectl apply -f common/default-server-secret.yaml

Create a config map for customizing NGINX configuration:

$ kubectl apply -f common/nginx-config.yaml

Create custom resource definitions for VirtualServer and VirtualServerRoute resources:

$ kubectl apply -f common/custom-resource-definitions.yaml

Run ingress controller

$ kubectl apply -f deployment/nginx-ingress.yaml

Use a DaemonSet: When you run the Ingress Controller by using a DaemonSet, Kubernetes will create an Ingress controller pod on every node of the cluster

$ kubectl apply -f daemon-set/nginx-ingress.yaml

Check that the Ingress Controller is Running

$ kubectl get pods --namespace=nginx-ingress

#cert manager

Create namespace for cert manager

$ kubectl create namespace cert-manager

$cd /cert-manager

$kubectl apply -f cert-manager.yaml

#Task 3 Application 

#I have provided the docker file need to create docker image from that and run container using that docker image.






