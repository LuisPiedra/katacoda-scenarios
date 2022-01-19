Create a service for exposing the deployment.

`kubectl expose deployment/webapp --type="NodePort" --port 9898`{{execute}}

We use `NodePort` for accessing from outside the cluster, as `ClusterIP` would only provide a cluster internal IP. Be aware Load Balancer is not supported in this playground. `9898` in this case is the port wher applicaiton is listening.

The sercive appears in the cluster. There are two services because the `kubernetes` one is created by default.

`kubectl get services`{{execute}}

Find out what port has been exposed:

`kubectl describe services/webapp`{{execute}}

`export NODE_PORT=$(kubectl get services/webapp -o go-template='{{(index .spec.ports 0).nodePort}}')`{{execute}}

`echo NODE_PORT=$NODE_PORT`{{execute}}

In this case, as we use NodePort and the workwernode is actually `localhost`, the webapp is accesible at that port.

`curl http://localhost:${NODE_PORT}`{{execute}}
