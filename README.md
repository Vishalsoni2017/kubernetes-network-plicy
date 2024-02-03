![image](https://github.com/Vishalsoni2017/kubernetes-network-plicy/assets/76658874/7528c6ac-8a9b-4a95-8c52-1913c576d94d)
kubectl apply -f ./manifests/hello-app/
   14  cd manifests
   15  cd hellp-app
   16  ls
   17  cd hello-app
   18  ls
   19  cd
   20  ls
   21  clear
   22  kubectl get all
   23  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=hello)
   24  clear
   25  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=not-hello)
   26  kubectl apply -f ./manifests/network-policy.yaml
   27  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=not-hello)
   28  kubectl delete -f ./manifests/network-policy.yaml
   29  kubectl create -f ./manifests/network-policy-namespaced.yaml
   30  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=hello)
   31  kubectl -n hello-apps apply -f ./manifests/hello-app/hello-client.yaml
   32  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=hello)
   33  kubectl logs --tail 10 -f -n hello-apps $(kubectl get pods -oname -l app=hello -n hello-apps)
   34  history
