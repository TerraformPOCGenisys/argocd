
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

- create deployment files in "genisys" folder
- create argocd application file in "argocd-deployment"
- apply the file created in argocd-deployment folder