minikube 

https://github.com/kubernetes/minikube/issues/4540

$ minikube stop
$ minikube delete

$ brew cask uninstall minikube
$ rm -rf ~/.minikube ~/.kube
Go to https://www.virtualbox.org/wiki/Downloads, use VirtualBox_Uninstall.tool script provided in OS X host .dm file
Disconnect from VPN
Restart laptop, make sure that you are not reconnected to VPN
Install VirtualBox using VirtualBox.pkg from the same .dmg file as the previous step.
$ brew cask install minikube
$ minikube start --alsologtostderr -v=9
Connect to VPN (if you wish)
--------------
npm install

touch Dockerfile

touch .dockerignore

docker build -t shussey/app-in-docker .

docker images

docker run -p 49160:8080 -d shussey/app-in-docker

docker ps

docker logs <container id>

curl -i localhost:49160

docker login

https://kubernetes.io/docs/tasks/run-application/run-stateless-application-deployment/

kubectl apply -f deployment.yaml

kubectl get deployments

kubectl describe deployment sjh-app1

kubectl get pods -l app=sjh-app1

kubectl apply -f service.yaml

kubectl get services

kubectl describe service sjh-app1-service

get the external IP of minikube
minikube ip 

use the service NodePort

curl http://$(minikube ip):31364
