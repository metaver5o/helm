# helm
**storing helm charts** <br><br>
`helm init` <br>
`kubectl create serviceaccount --namespace kube-system tiller` <br>
`kubectl create clusterrolebinding tiller-cluster-rule --clusterrole=cluster-admin --serviceaccount=kube-system:tiller` <br>
`kubectl patch deploy --namespace kube-system tiller-deploy -p '{"spec":{"template":{"spec":{"serviceAccount":"tiller"}}}}'` <br>
