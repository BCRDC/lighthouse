docker-compose up --force-recreate --no-deps --build lighthouse



# config map
https://carlos.mendible.com/2019/02/10/kubernetes-mount-file-pod-with-configmap/


# where is config detail
https://getakka.net/articles/configuration/akka.cluster.html

kubectl get configmaps bccs-cluster  -o yaml --namespace bccs

kubectl create configmap bccs-cluster --namespace bccs --from-file=akka.hocon=D:\backup\lighthouse\src\aks\akka.hocon


# how to mount one file from configmap
https://stackoverflow.com/questions/33415913/whats-the-best-way-to-share-mount-one-file-into-a-pod


#configmap how to replace
https://stackoverflow.com/questions/38216278/update-k8s-configmap-or-secret-without-deleting-the-existing-one


# foreach node
kubectl get nodes -o name

kubectl label nodes node/aks-agentpool-25762600-0 app=akka.node01



# use external network
https://stackoverflow.com/questions/46461977/docker-compose-v3-static-ip

docker network create --subnet 10.5.0.0/24 local_network_dev



# how to pass env as yaml content

https://github.com/kubernetes/kubernetes/issues/57726


sample : https://github.com/kubernetes/kubernetes/blob/master/cluster/addons/fluentd-elasticsearch/es-statefulset.yaml