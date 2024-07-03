
####  project on console
- login with argocd
- go to setting ->project
- inside default project -> go to role -> add role ->
Action Application     permission
*       default/*     allow

- and create the role


##### coonection with github
go to setting -> repository -> add repository

###### now deploy the application

- first create secret in argocd namespace
kubectl --namespace argocd create secret generic git-creds --from-literal=username=chanduksv --from-literal=password="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"



###### deploying application

- create deployment files in "argocd-deployment-files"
- create argocd application file in "argocd-application"
- apply the file created in argocd-application folder