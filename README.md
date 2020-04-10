# helm-charts
This repo consist of 2 helm charts.
* http-api-operator for launching an http-api-operator and a nginx server.
* http-api for creating 2 HTTP apis.

# Runbook
In the following commands replace the <variable-names> with your own variable names.

* To add this helm repo to your local repositories, run
```helm repo add <http-api-helm-charts> https://vijtrip2.github.io/helm-charts/```

* To install http-api-operator, run 
```helm install <http-api-operator> <http-api-helm-charts>/http-api-operator --set serviceAccount.annotations."eks\.amazonaws\.com/role-arn"='<arn:aws:iam::309117047740:role/RoleForK8sCluster>',serviceAccount.name=<apigateway-serviceaccount>```
The role and service account should match the role and trust relationship you set for IRSA.

* To install 2 sample HTTP apis, run
```helm install <http-api> <http-api-helm-charts>/http-api```
