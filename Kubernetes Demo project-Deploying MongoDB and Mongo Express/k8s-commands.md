# kubectl apply commands in order
    
    kubectl apply -f mongo-secret.yaml
    kubectl apply -f mongo.yaml
    kubectl apply -f mongo-configmap.yaml 
    kubectl apply -f mongo-express.yaml

# kubectl get commands

    kubectl get pod
    kubectl get pod --watch
    kubectl get pod -o wide
    kubectl get service
    kubectl get secret
    kubectl get all | grep mongodb # get all components details, search by mongodb

# kubectl debugging commands

    kubectl describe pod mongodb-deployment-<>
    kubectl describe service mongodb-service
    kubectl logs mongo-express-<>

# Give a URL/public IP address to external service in minikube

    minikube service mongo-express-service