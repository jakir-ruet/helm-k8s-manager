### Deploy with Helm

```bash
helm install nodejs-three-tier helm/nodejs-three-tier-app -n nodejs-app --create-namespace
kubectl get pods,svc,ingress -n nodejs-app
minikube tunnel
http://nodejs.local
```

### Verify Database Connection

```bash
kubectl exec -it deployment/backend -n nodejs-app -- sh
ping mysql
```
