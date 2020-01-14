# Expose
## Commandes de base

``kubectl expose deployment/nginx``   
 

Pour modifier une configuration existante dans un cluster, vous pouvez utiliser les 
sous-commandes **apply**, **edit** ou **patch** pour faire un correctif sans arreter le pod.  
La commande **apply** effectue un diff entre les precedentes modifications, 
la version actuelle et les modifications en cours, les champs non mentionnés ne sont pas affectés.   
**Edit** effectue d'abord un commande get, ouvre un éditeur, puis applique les modifications.  
Vous pouvez mettre à jour des objets API  avec la commande **patch** et passer un script JSON.  
Si la configuration comporte des champs *ressource* qui ne peuvent pas être mis à jour une fois initialisés, 
une mise à jour "forcée" peut être effectuée.
en utilisant l'option ``replace --force``. Cela supprime d'abord, puis recrée une ressource.

``kubectl replace -f second_with_expose.yaml``  
    
Voir le mise a jour en verifiant la colonne AGE    

``kubectl get deploy,pod``
  
Relancer avec expose  

``kubectl expose deployment/nginx``