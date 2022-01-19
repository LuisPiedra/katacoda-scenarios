Create a deployment with kubectl command.

`kubectl create deployment webapp --image=gcr.io/google-samples/kubernetes-bootcamp:v1`{{execute}}

And the deployment appears in the cluster.

`kubectl get deployments`{{execute}}

This deployment will create ReplicaSet, with will in turn create the pod:

`kubectl get replicasets`{{execute}}

`kubectl get pods`{{execute}}
