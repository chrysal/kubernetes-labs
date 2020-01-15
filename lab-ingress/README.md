# lab Ingress
##Installation avec helm 
```shell script
    helm install nginx-ingress --set rbac.create=true stable/nginx-ingress
```
## Installer le code source
```shell script
  git clone https://github.com/nginxinc/kubernetes-ingress/
  git checkout v1.6.0
  cd kubernetes-ingress/deployments
  # create namespace and service account
  k apply -f common/ns-and-sa.yml
  # create clusterrole et clusterrolebinding
  k apply -f rbac/rbac.yaml
  # Create a secret with TLS certificate 
  k apply -f common/default-server-secret.yaml
  # create a config map 
  k apply -f common/nginx-config.yaml
  # create a resource definitions for virtualer Server and virtual route
  K apply -f common/custom-resource-definitions.yaml
  # Deploy the ingress controller
  k apply -f deployment/nginx-ingress.yaml
  # ou utiliser  un Daemonset 
  k  apply -f daemon-set/nginx-ingress.yaml
```
Check 
```shell script
    kget pods --namespace=nginx-ingress
```



