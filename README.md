mac
### Init setup
https://argo-cd.readthedocs.io/en/stable/getting_started/
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
brew install argocd
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
kubectl port-forward svc/argocd-server -n argocd 8080:443
argocd admin initial-password -n argocd
argocd login 10.1.0.14:8080


kubectl apply -f /Users/sshabir/Documents/GitHub/kafkaconnect/argoCD/application.yaml



# install ArgoCD in k8s
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# access ArgoCD UI
kubectl get svc -n argocd
kubectl port-forward svc/argocd-server 8080:443 -n argocd

# login with admin user and below token (as in documentation):
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo

# you can change and delete init password


xG9J6dEVApcS2ofB

argocd app sync myapp --local /Users/sshabir/Documents/GitHub/kafkaconnect
    repoURL: "file:///Users/sshabir/Documents/GitHub/kafkaconnect"
    targetRevision: ''
    path: argoCD/myapp

argocd login argocd-server-5d8d58455f-5zc74
kubectl apply -f /Users/sshabir/Documents/GitHub/kafkaconnect/argoCD/application.yaml



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



