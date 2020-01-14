# Simple App
## Commandes de base

``kubectl create deployment nginx --image=nginx`` 

``kubectl describe deployment nginx``  

Pour voir la liste des actions faites precedement  
``kubectl get events``
Voir le resultat au format Yaml  
``kubectl get deployment nginx -o yaml``  
``kubectl get deployment nginx -o yaml > first.yaml``  
enlever les sections creationTimestamp, resourceVersion, selfLink et uid
et le bloc de lignes apres status:   
``kubectl delete deployment nginx`` 
recreer le deploiement a partir du fichier second.yaml  
``kubectl create -f second.yaml``

``kubectl get deployment nginx -o yaml > third.yaml``
faire un diff du second and third fichiers

 
