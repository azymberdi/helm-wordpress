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
  * #Inside value-yaml, change the namespace to yours. Default is azym-task.
  * helm install wordpress-mysql-helm-chart
  * kubectl get service -n azym-task 
  * #Get the load balancer IP and paste it on the Internet Browser
 
  
  
  
