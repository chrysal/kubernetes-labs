# LAB 1
## Commandes de base

``kubectl get nodes`` 
 
Resultat  
``NAME                   STATUS   ROLES    AGE   VERSION``  
``k8s-cluster-1-master   Ready    master   25h   v1.15.3``    
``k8s-cluster-1-node-1   Ready    <none>   25h   v1.15.3``  
``k8s-cluster-1-node-2   Ready    <none>   25h   v1.15.3``  
``k8s-cluster-1-node-3   Ready    <none>   25h   v1.15.3``  
  
`` kubectl describe node k8s-cluster-1-master``  
Affichage de la configuration du master
Explication sur la signification de la mesure : 170mi   
Verifier la valeur de Taints  
``node-role.kubernetes.io/master:NoSchedule``
Le master n'authorise pas les non-internals pods par defaut pour 
des raisons de securite. 
Nous allons authoriser l'utilisation des nodes master pour la formation
   
``kubectl describe node | grep -i taint``  
Resultat:   
``Taints:             node-role.kubernetes.io/master:NoSchedule``  
``Taints:   <none>``  
``Taints:             <none>``  
``Taints:             <none>``   
Commande pour enlever le Taint, attention a caractere - a la fin de la ligne  
``kubectl taint nodes --all node-role.kubernetes.io/master-``
  
Verifier si le DNS et Calico pods sont ok  
``kubectl get pods --all-namespaces``  