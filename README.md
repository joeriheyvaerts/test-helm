# test-helm

Create a package from your helm chart ( could be multiple charts )
```bash
helm package <dir>
``` 

Create a index file for your charts

```bash
helm repo index . --url <url location of your packages>
```
Place the index.yaml and tgz files on your webserver ( github, S3, ... )

Get repo on your instance

```bash
helm repo add hop-server <url location> (http://<bucketname>.s3-website-eu-west-1.amazonaws.com)
```

Install Chart
options:
- debug --debug
- version --version ( if you don't want to use the latest package/chart
```bash
helm install hop hop-server/hop-server
```

Kubectl

get deployments or pods
```bash
kubectl get deployments
kubectl get pods
```


