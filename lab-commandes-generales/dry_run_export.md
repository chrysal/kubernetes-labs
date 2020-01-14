# Dry_run and Export 
## Commandes de base

``kubectl create deployment two --image=nginx --dry-run -o yaml`` 
il n'y a pas les informations que l'on a enlevees precedement 
mais la valeur de la version d'apiVersion differe.    
yaml  
``kubectl get deployments nginx --export -o yaml``  
ou json  
``kubectl get deployments nginx --export -o json``  


 
