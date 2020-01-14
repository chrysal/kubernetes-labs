# Replicas
 
## Commandes de base

``kubectl get deployment nginx``  

Augmenter le nombre de servers de 1 a 3  

``kubectl scale deployment nginx --replicas=3``  

Verifier les endpoints.   

``kubectl get ep nginx`` 

 supprimer le pod le plus ancien  
 ``kubectl git po -o wide``  
 
 ``kubectl delete po nginx-<valeur>``   
 Check   
 ``kubectl get ep nginx`` 
 
 
 
 


 
