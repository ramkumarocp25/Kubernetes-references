## Install and setup Helm Package Manager

```
wget https://storage.googleapis.com/kubernetes-helm/helm-v2.12.2-linux-amd64.tar.gz
tar -zxvf helm-v2.12.2-linux-amd64.tar.gz
sudo mv linux-amd64/helm /usr/local/bin/helm
kubectl -n kube-system create sa tiller
kubectl create clusterrolebinding tiller --clusterrole cluster-admin --serviceaccount=kube-system:tiller
helm init --service-account tiller

```
https://daemonza.github.io/2017/02/20/using-helm-to-deploy-to-kubernetes/

https://opensource.com/article/20/5/helm-charts
