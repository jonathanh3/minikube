# Simple pod example

```shell
kubectl run test-app --image=nginx --restart=Never

kubectl port-forward my-pod 8080:80 # to access the web app on the localhost:8080
```
