# Port forwarding

To access ArgoCD UI after restarting:

```bash
kubectl port-forward svc/argocd-server -n argocd 8080:443 --address=0.0.0.0 &
```

To access Prometheus metrics:

```bash
kubectl port-forward svc/kube-prometheus-stack-prometheus -n monitoring 9090:9090 --address=0.0.0.0 &
```

To access Grafana:

```bash
kubectl port-forward svc/kube-prometheus-stack-grafana -n monitoring 3000:80 --address=0.0.0.0 &
```