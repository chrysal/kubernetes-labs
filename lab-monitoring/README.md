# lab montoring with Prometheus
## installation 
```shell script
   git clone https://github.com/cesigit/kubernetes-prometheus.git
   cd kubernetes-prometheus
   k create namespace monitoring
   k create -f clusterRole.yaml
   k create -f config-map.yaml 
   k create -f prometheus-deployment.yaml 
```
Attendre quelques temps avant d'obtenir des metriques  
```shell script
    k top nodes 
    k top pods 
``` 
 