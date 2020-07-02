# helm-wordpress (installed with helm v2)

Commands:
  * helm version
  * sudo mv /usr/local/bin/helm  /usr/local/bin/helm3
  * wget https://get.helm.sh/helm-v2.16.9-linux-amd64.tar.gz
  * tar -xf helm-v2.16.9-linux-amd64.tar.gz
  * sudo mv linux-amd64/helm /usr/local/bin/helm
  * helm version
  * kubectl create sa -n kube-system tiller
  * kubectl create clusterrolebinding tiller-cluster-admin --clusterrole=cluster-admin --serviceaccount=kube-system:tiller
  * helm init --service-account tiller --upgrade
  * cd helm-wordpress/
  * helm install wordpress-mysql-helm-chart
  * kubectl get service -n azym-task # this is to get the NodePort, 32237 in my case
  * kubectl get nodes -o wide
  
* Dont forget to change the namespace name in values file.

Adnan's notes (did not want to delete)
  
  * create chart named "wp"
  * go to the directory and execute that command
  * helm install  --name wp --values values.yaml .
  * if you want to use a repository with your pre-configured "values.yaml" file; 
  * helm install  --name wp --values values.yaml stable/wordpress
  * kubectl get pods -n azym-task
  * kubectl get service -n azym-task
  
  
