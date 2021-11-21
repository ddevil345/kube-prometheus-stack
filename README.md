# Install kube-prometheus-stack with Helm pv,pvc on NFS
- Cteate ns monitoring

user@k8s:~$ kubectl create namespace monitoring

- Create pv and pvc

user@k8s:~$ kubectl apply -f create-pv-pvc.yaml

- Install.

user@k8s:~$ helm install prometheus prometheus-community/kube-prometheus-stack --values values.yaml -n monitoring

- default user/pass
- admin/prom-operator
