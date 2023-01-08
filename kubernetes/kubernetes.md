Kubernetes project.

1) Create a docker  image  called "demo-pod"  on local machine.
2) give a tag called "v1" i.e demo-pod:v1
3) Push docker image called "demo-pod" to your own registyr registry (public registry)
4) Create deployment file (https://kubernetes.io/docs/concepts/workloads/controllers/deployment/ )and use your own container image inside deployment with 2 replicas in demo namespace
5) apply that (kubectl apply -f <deployment.yaml>) .yaml file and check if deployment and pods is/are running and what images/tag deployment using. 
    
    verification:
    
    kubectl get deployment -n demo
    
    kubectl get pods -n demp
    
    kubectl scale  --replicas=<number>  deployment <deployment-name>
    
    kubectl describe pod <pod-name> | grep -i "image"  
