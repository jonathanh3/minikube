# Kubernetes Dashboard

To deploy the Kubernetes Dashboard:

```shell
# Add kubernetes-dashboard repository
helm repo add kubernetes-dashboard https://kubernetes.github.io/dashboard/
# Deploy a Helm Release named "kubernetes-dashboard" using the kubernetes-dashboard chart
helm upgrade --install kubernetes-dashboard kubernetes-dashboard/kubernetes-dashboard --create-namespace --namespace kubernetes-dashboard
```

Command line proxy:

```shell
kubectl -n kubernetes-dashboard port-forward svc/kubernetes-dashboard-kong-proxy 8443:443
```

Pull the chart:

```shell
helm pull kubernetes-dashboard/kubernetes-dashboard --untar --untardir
```

## Uninstall

```shell
helm uninstall kubernetes-dashboard
```

## Minikube Dashboard

```shell
minikube dashboard start
```
