# Service 
## Commandes de base

``kubectl get svc nginx``  
Attention the cluster-ip n'est pas le endpoint. Calico est le cluster-IP a partir
duquel le endpoint est maintenu par le *kubelet* et *kube-proxy*
   
``kubectl get ep nginx``  
permet d'obtenir l'adresse IP du endpoint. 

Connaitre le node ou nginx est deploye   
``kubectl describe pod <pod_name> | grep Node:``  

A partir du master faire  
``curl <Cluster-IP>:80``  
ou  
``curl <IP adresse du endpoint>:80``


 
