Now, let's scale the deployment with multiple replicas:

`kubectl get deployments`{{execute}}

`kubectl scale deployments/kubernetes-bootcamp --replicas=3`{{execute}}

And now we have four pods running for the application

`kubectl get deployments`{{execute}}

`kubectl get pods -o wide`{{execute}} 

And each request can go to any of them:

`curl http://localhost:${NODE_PORT}`{{execute}}
