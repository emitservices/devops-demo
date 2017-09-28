## Hello-world Service
Latest service image is maintaied at docker.io/fawaz/us.fetchr.sample:latest
In this section, the service will be launched and Orchestrated using kubernetes on Google Container Engine.

To start the pod, run the below command:
```
kubertl apply -f hello-world.yml
```
To start the deployment, run the below command:
```
kubertl apply -f hello-world-deployment.yml
```
To start the service, run the below command:
```
kubectl apply -f hello-world-service.yml
```
Then, see the assigned public IP address to access the service:
```
kubectl get services hello-world
```
The output should look like:
```
NAME          CLUSTER-IP      EXTERNAL-IP      PORT(S)        AGE
hello-world   10.39.246.129   35.202.209.228   80:31283/TCP   34m
```
![Logo](images/hello-world-service.png)
