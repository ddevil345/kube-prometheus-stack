# Install kube-prometheus-stack with Helm pv,pvc on NFS
- Cteate ns monitoring

kubectl create namepsace monitoring

- Create pv and pvc

kubectl apply -f create-pv-pvc.yaml

- Install.

helm install prometheus prometheus-community/kube-prometheus-stack --values values.yaml -n monitoring

- default user/pass
- 
admin/prom-operator
