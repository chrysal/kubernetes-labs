# lab Job
## installation 
Alors que la plupart des applications sont déployées de telle sorte qu'elles continuent a etre disponibles,  
il y a certaines que nous souhaitons pouvoir exécuter un certain nombre de fois, elles sont appelées ```Job```,    
d'autres applications peuvent etre executees regulierement, toutes les heures ou tous les jours; elles sont ainsi appelées ```CronJob```.

```shell script
   k create -f job.yaml
   k get job 
   k describe jobs.batch sleepy
``` 
Supprimer le job   
``` k delete jobs.batch sleepy ```

