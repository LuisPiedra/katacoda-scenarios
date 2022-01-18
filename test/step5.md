`kubectl get deployments`{{execute}}
`kubectl get replicasets`{{execute}}
`kubectl get pods -o wide`{{execute}}
`kubectl set image deployments/kubernetes-bootcamp kubernetes-bootcamp=jocatalin/kubernetes-bootcamp:v2`{{execute}}
`kubectl get pods -o wide`{{execute}}
`kubectl get replicasets`{{execute}}
`kubectl rollout undo deployments/kubernetes-bootcamp`{{execute}}
