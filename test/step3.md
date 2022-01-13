Create a pod with declarative commands

`cat example/pod.yaml`{{execute}}
`kubectl apply -f example/pod.yaml`{{execute}}

List pods

`kubectl get pod static-web`{{execute}}

Delete pods
`kubectl delete pod static-web`{{execute}}

List not empty
`kubectl get pod static-web`{{execute}}
