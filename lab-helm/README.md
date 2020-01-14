# Installer Helm
##Installation de binaire
```shell script
   wget https://get.helm.sh/helm-v3.0.2-linux-amd64.tar.gz
   tar -zxvf helm-v3.0.2-linux-amd64.tar.gz
   cd linux-amd64/
   sudo mv helm /usr/local/bin/helm
   helm help
```
## Cherche un chart dans le repository hub 
``` helm search hub wordpress```  

## ajouter un repo et installer mysql  chart
```shell script
    helm repo add stable https://kubernetes-chart.storage.googleapis.com```
    helm search repo stable
    helm repo update
    k create -f mysqldb-hostpath.yaml
    k get pv
    k create -f mysqldb-pvc.yaml
    k get pvc
    helm install  mysql --set mysqlRootPassword=rootpassword,mysqlUser=mysql,mysqlPassword=my-password,mysqlDatabase=mydatabase,persistence.existingClaim=mysql-pvc stable/mysql
    k get pod
    watch k get pod
    watch kubectl get pod
```
