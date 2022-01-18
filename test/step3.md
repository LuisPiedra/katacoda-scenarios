Create a service. Be aware Load Balancer is not supported in this playground

`kubectl get services`{{execute}}
`kubectl expose deployment/kubernetes-bootcamp --type="NodePort" --port 8080`{{execute}}
`kubectl get services`{{execute}}

Find out what port has been exposed
`kubectl describe services/kubernetes-bootcamp`{{execute}}

`export NODE_PORT=$(kubectl get services/kubernetes-bootcamp -o go-template='{{(index .spec.ports 0).nodePort}}')`{{execute}}
`echo NODE_PORT=$NODE_PORT`{{execute}}

`curl http://localhost:${NODE_PORT}`{{execute}}
