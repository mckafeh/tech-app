# tech-app

Building the Docker image
$ docker build --tag django_todo:latest .

Test running the the Docker container
$ docker run --name hello-world-app -d -p 8000:8000 hello-world-app:latest


Publishing the Docker image to Docker Hub

$ docker login
$ docker tag hello-world-app:latest mckafeh/hello-world-app:latest
$ docker push mckafeh/hello-world-app:latest

Runing the App on Minikube

kubectl create deployment hello-world-app --image=mckafeh/hello-world-app
kubectl expose deployment hello-world-app --type=LoadBalancer --port=8080