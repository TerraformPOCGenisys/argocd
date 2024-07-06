
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
## login to cluster
aws eks --region ap-south-1 update-kubeconfig --name eks-stag-poc
- first create secret in argocd namespace
kubectl --namespace argocd create secret generic git-creds --from-literal=username=dhruv.p@genisys-group.com 
 --from-literal=password="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"



###### deploying application

- create deployment files in "genisys" folder
- create argocd application file in "argocd-deployment"
- apply the file created in argocd-deployment folder
        kubectl apply -f frontend.yaml
-if cluster is created new than run ingress also
        kubectl apply -f ingress.yaml