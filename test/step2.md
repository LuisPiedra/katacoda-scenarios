Create a pod with imperative commands

`kubectl run pod1 --image=nginx`{{execute}}

Create another pod

`kubectl run pod2 --image=nginx`{{execute}}

List pods

`kubectl get pods`{{execute}}

Get pod details

`kubectl get pod pod1`{{execute}}

Get more details

`kubectl get pod pod1 -o yaml`{{execute}}

Cleanup
`kubectl delete pod1 pod2`{{execute}}

List empty
`kubectl get pods`{{execute}}
