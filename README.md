# flask_kubernetes_using_nginx_ingress

1) Using the Dockerfile first build the image :

docker build -t="flask_app_with_ingress" .



2) Create Deployment :

kubectl apply -f flask-deployment.yml 



3) Create Service :

kubectl apply -f flask-services.yml




4) Apply ingress :

kubectl apply -f flask-ingress.yml  





5) Enable ingress in minikube :

minikube addons enable ingress





6) Access the app :

10:56AM @Bharath ~ curl -i http://192.168.49.2
HTTP/1.1 200 OK
Date: Sat, 13 Aug 2022 17:56:48 GMT
Content-Type: text/html; charset=utf-8
Content-Length: 77
Connection: keep-alive

This is a test webseite ! and served by host: flaskdeployment-5495c4b45-b4jkc
