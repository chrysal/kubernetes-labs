# Acces depuis l'exterieur 
## Commandes de base

Obtenir la liste des pods  
``kubectl get po``

Choisir un pod et faire un exec dessus  
``kubectl exec nginx-<pod_number> -- printenv |grep KUBERNETES``

delete the service  
``kubectl delete svc nginx``  

Creer a nouveau le service mais avec le type loadbalancer  
``kubectl expose deployment nginx --type=LoadBalancer``  
et faire  
``kubectl get svc``  
Vous avez acces au site web nginx avec l'IP public de votre master et le port 3xxxx  
Mettre le deploiement a zero replica  
 ``kubectl scale deployment nginx --replicas=0``  
Demarrer 2 replicas   
``kubectl scale deployment nginx --replicas=2``  
Detruire le deploiement pour recuperer les ressources 
``kubectl delete deployments nginx``
mais attention les endpoints et le service restent orphelins  
faire   
``kubectl delete ep nginx``  
et  
``kubectl delete svc nginx``  






 
