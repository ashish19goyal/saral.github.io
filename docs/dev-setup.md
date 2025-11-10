# Working with minikube
- minikube start --profile=saral-test --memory=7240 --disk-size=30g --kubernetes-version=v1.26.1 --driver=docker --ports=8080:80 --ports=8443:443 --ports=30080:30080 --ports=30443:30443
- minikube start -p saral: To create a minikube profile
- minikube profile saral: To set minikube profile
- minikube config get profile: To get minikube profile
- eval $(minikube -p {profile} docker-env): to set minikube as docker env


# Working with kubectl
- kubectl get: shows information about an object
- kubectl describe: shows more detailed info about an object
- kubectl logs: displays log output from containers
- kubectl explain: shows what fields are available when declaring an object
- kubectl config get-contexts: to list all available profiles
- kubectl config view --minify | grep namespace: to check current namespace
- kubectl get pods --watch: to see all the pods running in k8s cluster

# Pushing images to GCP
- tag the image: docker tag {image-full-name} asia-south1-docker.pkg.dev/saral-450313/saral-docker-repo/{image-name}:{tag}
- push image: docker push asia-south1-docker.pkg.dev/saral-450313/saral-docker-repo/{image-name}:{tag}
- pull image: docker pull asia-south1-docker.pkg.dev/saral-450313/saral-docker-repo/{image-name}:{tag}