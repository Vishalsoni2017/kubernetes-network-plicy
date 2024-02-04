![image](https://github.com/Vishalsoni2017/kubernetes-network-plicy/assets/76658874/7528c6ac-8a9b-4a95-8c52-1913c576d94d)
<br>kubectl apply -f ./manifests/hello-app/<br>
   14  cd manifests<br>
   15  cd hellp-app<br>
   16  ls<br>
   17  cd hello-app<br>
   18  ls<br>
   19  cd<br>
   20  ls<br>
   21  clear<br>
   22  kubectl get all<br>
   23  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=hello)<br>
   24  clear<br>
   25  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=not-hello)<br>
   26  kubectl apply -f ./manifests/network-policy.yaml<br>
   27  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=not-hello)<br>
   28  kubectl delete -f ./manifests/network-policy.yaml<br>
   29  kubectl create -f ./manifests/network-policy-namespaced.yaml<br>
   30  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=hello)<br>
   31  kubectl -n hello-apps apply -f ./manifests/hello-app/hello-client.yaml<br>
   32  kubectl logs --tail 10 -f $(kubectl get pods -oname -l app=hello)<br>
   33  kubectl logs --tail 10 -f -n hello-apps $(kubectl get pods -oname -l app=hello -n hello-apps)<br>
   34  history
<br>
