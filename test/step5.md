Now, lets do and update in the applicaiton version, by just telling the deployment to use a new image:
`kubectl set image deployments/webapp podinfo=stefanprodan/podinfo:6.0.3`{{execute}}

This will create a new replica set, and update the desired replica count:

`kubectl get replicasets`{{execute}}

Which will destroy old pods and create new ones:

`kubectl get pods -o wide`{{execute}}

In the same way, we can go back to the previous replicaset:

`kubectl rollout undo deployments/webapp`{{execute}}
