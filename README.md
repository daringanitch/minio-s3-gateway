# minio-s3-gateway tested on KOPS deployed Kuberenetes cluster in AWS

kubernetes install using helm charts and  custom values.yaml

1. clone repo to local

2. Create a AWS user and substitute security keys  in the values.yaml. User should have s3 access rights.

  AWS_ACCESS_KEY_ID: "thekey"
  AWS_SECRET_ACCESS_KEY: "thesecret"
  
  
  values.yaml as is will create a 4 pod gateway deployment with s3 as the backend and a LoadBalancer.
  
  explore many other options in the values.yaml. Refer to https://doc.minio.io/ for more information.
  
 3. use following command after editing vaules.yaml file

### helm install --name minio-s3-gateway  -f values.yaml stable/minio




