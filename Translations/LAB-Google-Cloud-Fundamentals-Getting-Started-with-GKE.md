# LAB: Google Cloud Fundamentals: Getting Started with GKE

## Objectives:

In this lab, you will learn how to perform the following tasks:

  - Provision a Kubernetes cluster using Kubernetes Engine.

  - Deploy and manage Docker containers using kubectl.


## Steps:

1. Start a Kubernetes Engine cluster.

        export MY_ZONE=us-central1-a

        gcloud container clusters create webfrontend --zone $MY_ZONE --num-nodes 2




2. Run and deploy a container.

        kubectl create deploy nginx --image=nginx:1.17.10

        kubectl get pods

        kubectl expose deployment nginx --port 80 --type LoadBalancer

        kubectl scale deployment nginx --replicas 3
