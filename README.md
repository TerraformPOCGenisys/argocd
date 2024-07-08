
####  project on console
- login with argocd
- go to setting ->project
- inside default project -> go to role -> add role ->
Action Application     permission
*       default/*     allow

- and create the role



##### coonection with github
go to setting -> repository -> add repository



###### deploying application

- create deployment files in "genisys" folder
- create argocd application file in "argocd-deployment"
- apply the file created in argocd-deployment folder
        kubectl apply -f frontend.yaml
-if cluster is created new than run ingress also
        kubectl apply -f ingress.yaml
