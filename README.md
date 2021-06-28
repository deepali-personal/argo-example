helm repo add argo-cd https://argoproj.github.io/argo-helm

helm dep update charts/argo-cd/

# Display the current Context:
    kubectl config current-context

# List all the Contexts in a kubeconfig file:
    kubectl config get-contexts

minikube start --driver=hyperv --memory 8192 --cpus 6

# Switch Context:
    kubectl config use-context <context_name>


helm upgrade --install argo-cd charts/argo-cd/

Referred Links
https://www.arthurkoziel.com/setting-up-argocd-with-helm/
