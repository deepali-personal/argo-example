helm repo add argo-cd https://argoproj.github.io/argo-helm

helm dep update charts/argo-cd/

# Display the current Context:
    kubectl config current-context

# List all the Contexts in a kubeconfig file:
    kubectl config get-contexts

minikube start --driver=hyperv --memory 8192 --cpus 6

# Switch Context:
    kubectl config use-context <context_name>

# For Argo related setup
helm upgrade --install argo-cd charts/argo-cd/

kubectl port-forward svc/argo-cd-argocd-server 8080:443

URL : http://localhost:8080
Username : admin
Password : [kubectl get pods -l app.kubernetes.io/name=argocd-server -o name]


helm template apps/ | kubectl apply -f -

Referred Links
https://www.arthurkoziel.com/setting-up-argocd-with-helm/
