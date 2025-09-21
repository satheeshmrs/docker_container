## Upgrade

kubectl set image deployment/kodekloudapp kodekloudappcs=crkode.azurecr.io/kodekloudapps:v2

## Reverse the deployment

kubectl rollout history deplopyment/kodekloudapp

kubctl rollout undo deployment/kodekloudapp

## 
