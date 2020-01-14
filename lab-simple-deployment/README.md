# Lab simple deployment 
Create a pod does not take advantage of orchestration abilities of kubernetes.  
When creating a Deployment you get scalability, reliability and updates. 

```shell script 
   k create deployment firstpod --image=nginx 
```
Check 
```shell script
    k get deploy,pod
    k describe pod firstpod-xxxx
```
The resources are in the default namespace 
```shell script
    k get namespaces
```
Look at the pods in kube-system namespace 
```shell script
    k get pod -n kube-system 
```
View all resources in all namespaces at once with --all-namespaces or -A
```shell script
   k get pod --all-namespaces 
   k get pod -A
```
How to see the yaml of the deployment
```shell script
    k get deployment firstpod -o yaml
    # save as a file
    k get deployment firstpod -o yaml > first.yaml 
```







View several resources at once. Note that most resources have a short name such as rs for ReplicaSet, po for Pod,
svc for Service, and ep for endpoint. Note the endpoint still exists after we deleted the pod.
```shell script
   k get deploy,rs,po,svc,ep
```

