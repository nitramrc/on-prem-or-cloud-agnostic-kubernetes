# install nginx ingress

```
helm install --name my-ingress stable/nginx-ingress \
  --set controller.kind=DaemonSet \
  --set controller.service.type=NodePort \
  --set controller.hostNetwork=true
```

# start myapp

Create myapp and add an ingress rule:

```
kubectl create -f myapp.yml
kubectl create -f myapp-ingress.yml
```

# install cert-manager

```
helm install \
    --name cert-manager \
    --namespace kube-system \
    stable/cert-manager
```


# New versions ...
```
url -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
   14  chmod +x get_helm.sh 
   15  ./get_helm.sh 
   16  cd on-prem-or-cloud-agnostic-kubernetes/helm/
   17  cat README.md 
   18  ls -la
   19  helm repo add stable https://charts.helm.sh/stable
   20  helm repo list
   21  cd ..
   22  cd cert-manager/
   23  ls -la
   24  cat README.md 
   25  helm install --name my-ingress stable/nginx-ingress   --set controller.kind=DaemonSet   --set controller.service.type=NodePort   --set controller.hostNetwork=true
   26  helm install my-ingress stable/nginx-ingress   --set controller.kind=DaemonSet   --set controller.service.type=NodePort   --set controller.hostNetwork=true
   27  helm list
   28  helm delete my-ingress
   29  helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
   30  helm repo update
   31  helm install my-ingress ingress-nginx/ingress-nginx --set controller.kind=DaemonSet   --set controller.service.type=NodePort   --set controller.hostNetwork=true
   32  helm list
   33  kubectl get node
   34  kubectl get pod
   35  kubectl get pod -o wide
   36  kubectl edit pod my-ingress-ingress-nginx-controller-pnv8q
   37  git status
   38  git pull --all
   39  git checkout nitram
   40  dig myapp.overbinary.org
   41  git pull origin nitram
   42  git pull origin nitram
   43  kubectl create -f myapp.yml 
   44  kubectl create -f myapp-ingress.yml 
   45  curl myapp.overbinary.org
   46  helm repo add jetstack https://charts.jetstack.io
   47  helm repo update
   48  helm install   cert-manager jetstack/cert-manager   --namespace cert-manager   --create-namespace   --version v1.7.1
   49  helm list
   50  kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.7.1/cert-manager.crds.yaml
   51  helm install   cert-manager jetstack/cert-manager   --namespace cert-manager   --create-namespace   --version v1.7.1
   52  helm list -n cert-manager
   53  helm delete cert-manager -n cert-manager
   54  helm install   cert-manager jetstack/cert-manager   --namespace cert-manager   --create-namespace   --version v1.7.1
   55  git pull origin nitram
   56  kubectl create -f issuer-staging.yml 
   57  git pull origin nitram
   58  kubectl create -f issuer-staging.yml 
   59  git pull origin nitram
   60  kubectl create -f issuer-staging.yml 
   61  kubectl create -f issuer-prod.yml 
   62  history 
   63  kubectl create -f certificate-staging.yml 
   64  kubectl create -f certificate-prod.yml 
   65  curl myapp.overbinary.org
   66  history 
   67  kubectl delete -f issuer-staging.yml
   68  kubectl delete -f issuer-prod.yml 
   69  kubectl delete -f certificate-staging.yml 
   70  kubectl delete -f certificate-prod.yml 
   71  history 
   72  git pull origin nitram
   73  kubectl create -f issuer-staging.yml 
   74  kubectl create -f certificate-staging.yml 
   75  kubectl apply -f myapp-ingress.yml 
   76  kubectl apply -f myapp-ingress.yml 
   77  kubectl apply -f myapp.yml 
   78  kubectl apply -f myapp.yml 
   79  curl myapp.overbinary.org
   80  curl https://myapp.overbinary.org
   81  history
```