# docker-learning
This is the course note from [**Introduction to Containers w/ Docker, Kubernetes &amp; OpenShift**](https://www.coursera.org/learn/ibm-containers-docker-kubernetes-openshift/ungradedLti/kgtxc/hands-on-lab-introduction-to-containers-docker-and-ibm-cloud-container-registry)

`docker --version`

`docker images` : check images list

`docker pull [image file]` : pull image from registry

`docker run -p 8080:80 [image file]`  ng : run the image as a container

`docker ps -a` list all containers

`docker container rm <container_id>`

In Dockerfile:

*The FROM instruction initializes a new build stage and specifies the base image that subsequent instructions will build upon.*

*The COPY command enables us to copy files to our image.*

*The RUN instruction executes commands.*

*The EXPOSE instruction exposes a particular port with a specified protocol inside a Docker Container.*

*The CMD instruction provides a default for executing a container, or in other words, an executable that should run in your container.*

### Docker build command

create a container image using the build command:

docker build -t my-app:v1

-t: tag   

my-app: repository   

v1:version

### Docker Commands

| Command | Description | Example |
| --- | --- | --- |
| curl localhost | Pings the application. | curl localhost |
| docker build | Builds an image from a Dockerfile. | docker build . |
| docker build . -t | Builds the image and tags the image id. | docker build . -t myimage:latest |
| docker CLI | Start the Docker command line interface. | docker |
| docker container rm | Removes a container. | docker container rm mycontainer |
| docker images | Lists the images. | docker images |
| docker ps | Lists the containers. | docker ps |
| docker ps -a | Lists the containers that ran and exited successfully. | docker ps -a |
| docker pull | Pulls the latest image or repository from a registry. | docker pull nginx:latest |
| docker push | Pushes an image or a repository to a registry. | docker push myimage:latest |
| docker run | Runs a command in a new container. | docker run ubuntu echo "Hello, world!" |
| docker run -p | Runs the container by publishing the ports. | docker run -p 8080:80 nginx |
| docker stop | Stops one or more running containers. | docker stop mycontainer |
| docker stop $(docker ps -q) | Stops all running containers. | docker stop $(docker ps -q) |
| docker tag | Creates a tag for a target image that refers to a source image. | docker tag myimage:latest myrepository/myimage:latest |
| docker –version | Displays the version of the Docker CLI. | docker --version |
| exit | Closes the terminal session. | exit |
| export MY_NAMESPACE=<namespace> | Exports a namespace as an environment variable. | export MY_NAMESPACE=mynamespace |

### Kubernetes Commands

| Command | Description | Example |
| --- | --- | --- |
| for …do | Runs a for command multiple times as specified. | for i in {1..5}; do echo $i; done |
| kubectl apply | Applies a configuration to a resource. | kubectl apply -f deployment.yaml |
| kubectl config get-clusters | Displays clusters defined in the kubeconfig. | kubectl config get-clusters |
| kubectl config get-contexts | Displays the current context. | kubectl config get-contexts |
| kubectl create | Creates a resource. | kubectl create deployment nginx --image=nginx |
| kubectl delete | Deletes resources. | kubectl delete pod mypod |
| kubectl describe | Shows details of a resource or group of resources. | kubectl describe pod mypod |
| kubectl expose | Exposes a resource to the internet as a Kubernetes service. | kubectl expose deployment nginx --port=80 --target-port=80 |
| kubectl get | Displays resources. | kubectl get pods |
| kubectl get pods | Lists all the Pods. | kubectl get pods |
| kubectl get pods -o wide | Lists all the Pods with details. | kubectl get pods -o wide |
| kubectl get deployments | Lists the deployments created. | kubectl get deployments |
| kubectl get services | Lists the services created. | kubectl get services |
| kubectl proxy | Creates a proxy server between a localhost and the Kubernetes API server. | kubectl proxy |
| kubectl run | Creates and runs a particular image in a pod. | kubectl run mypod --image=nginx |
| kubectl version | Prints the client and server version information. | kubectl version |

### Additional Kubernetes Commands

| Command | Description | Example |
| --- | --- | --- |
| kubectl autoscale deployment | Autoscales a Kubernetes Deployment. | kubectl autoscale deployment nginx --min=1 --max=5 --cpu-percent=80 |
| kubectl create configmap | Creates a ConfigMap resource. | kubectl create configmap myconfig --from-literal=key1=value1 |
| kubectl get deployments -o wide | Lists deployments with details. | kubectl get deployments -o wide |
| kubectl get hpa | Lists Horizontal Pod Autoscalers (hpa). | kubectl get hpa |
| kubectl scale deployment | Scales a deployment. | kubectl scale deployment nginx --replicas=3 |
| kubectl set image deployment | Updates the current deployment. | kubectl set image deployment/nginx nginx=nginx:1.9.1 |
| kubectl rollout | Manages the rollout of a resource. | kubectl rollout status deployment/nginx |
| kubectl rollout restart | Restarts the resource so that the containers restart. | kubectl rollout restart deployment/nginx |
| kubectl rollout undo | Rollbacks the resource. | kubectl rollout undo deployment/nginx |
