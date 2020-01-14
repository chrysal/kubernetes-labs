# Lab introduction 
# Basic commands
Creer un pod en ligne de commande  
``` kubectl run --generator=run-pod/v1 nginx --image=nginx```   
Creer un pod a partir d'un fichier YAML  
``kubectl create -f pod-definition.yaml``  
Verification  
``kubectl get pods``  
``kubectl describe pod myapp-pod``  

Comment generer du code yaml sans creer d'objet Kubernetes
``kubectl run --generator=run-pod/v1 nginx --image=nginx --dry-run -o yaml``
