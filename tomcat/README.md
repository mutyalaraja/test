Here i created two deployment file

1 first build images and deployment
2 Using persistance volume


Kubernetes Deployment File

To get the namespaces in kubernetes

kubectl get ns

To deploy the app in kuberentes

kubectl create -f app.yaml -n test
To deploy service

kubectl create -f ser.yaml -n test

To deploy ingress rule

kubectl create -f ing.yaml -n test

To check Pods running in respective namespace

kubectl get po -n test

To check the service running

kubectl get svc -n test

To check the ingress

kubectl get ing -n test
Other Method to deply in kuberbetes

kubectl run webapp \
  --image=imagename\
  --port=8080 -n test
To view the deployment you just created

kubectl get deployments -n test
To view the application instances created by the deployment

kubectl get pods -n test

Expose the service to external

kubectl expose deployment hello-java --type=LoadBalancer

To view the service created
