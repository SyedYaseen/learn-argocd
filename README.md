minikube start
minikube kubectl -- get pods

kubectl create namespace argocd
kubectl apply -n default -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

Port forwarding:
kubectl port-forward svc/argocd-server -n argocd 8080:443

.\argocd admin initial-password -n argocd
7mfCS2jXa7DmhslR

.\argocd login argocd-server-6b765cddc5-xg2d2 --username admin --password 7mfCS2jXa7DmhslR

kubectl apply -n default -f C:\Users\ssyed\Documents\Projects\Kubernetes\learn-argocd\application.yaml
