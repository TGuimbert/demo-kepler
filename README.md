# demo-kepler

```shell
kind create cluster --config ./local-cluster-config.yaml
kubectl apply --server-side -f kube-prometheus-manifests/setup
kubectl get servicemonitors --all-namespaces
kubectl apply -f kube-prometheus-manifests/
kubectl apply -f kepler-deployment.yaml
kubectl -n monitoring port-forward svc/grafana 3000
```

See [Electricity Maps](https://app.electricitymaps.com/zone/FR) for carbon emissions
