# helm-charts
This repo consist of 2 helm charts.
a) http-api-operator for launching an http-api-operator and a nginx server.
b) http-api for creating 2 HTTP apis.

In the following command replace the bold words with your own names.

To add this helm repo to your local repositories
helm repo add **http-api-helm-charts** https://vijtrip2.github.io/helm-charts/

To install http-api-operator, run 
helm install **http-api-operator** **http-api-helm-charts**/http-api-operator --set serviceAccount.annotations."eks\.amazonaws\.com/role-arn"=**'arn:aws:iam::309117047740:role/RoleForK8sCluster'**,serviceAccount.name=**apigateway-serviceaccount**


