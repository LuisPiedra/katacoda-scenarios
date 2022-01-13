Create a pod with imperative commands

`kubectl run pod1 --image=nginx`

Create another pod

`kubectl run pod2 --image=nginx`

List pods

`kubectl get pods`

Get pod details

`kubectl get pod pod1`

Get more details

`kubectl get pod pod1 -o yaml`

Cleanup
`kubectl delete pod1 pod2`

List empty
`kubectl get pods`
