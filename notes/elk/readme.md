# EFK

<h2>EFK Installation  </h2>

 Create a kind cluster to deploy EFK stack

```bash 
kind create cluster  --name=<cluster-name>
kubectl cluster-info --context <cluster-name>
```


<h2> ElasticSearch  Installation  </h2>

```bash 
kubectl apply -f elasticsearch.yaml

kubectl config set-context --current --namespace=kube-logging

Check the status of pods

kubectl get pods,svc -n kube-logging

Port-forward
kubectl port-forward svc/elasticsearch 9200:9200
 
Run these commands in new tab in terminal
curl 127.0.0.1:9200/
curl 127.0.0.1:9200/_cluster/health/?pretty
```

<h2> Kibana Installation </h2>

```bash
kubectl apply -f kibana.yaml

Check the status of pods

kubectl get pods,svc -n kube-logging

kubectl port-forward <kibana-pod-name> 5602:5601 

curl 127.0.0.1:5601/app/kibana

```


<h2> FluentD  Installation </h2>

```bash
kubectl apply -f fluentd.yaml

Check the status of pods

kubectl get pods,svc -n kube-logging
```

