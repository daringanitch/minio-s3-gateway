# minio-s3-gateway
kubernetes install using helm charts and  custom values.yaml

1. clone repo to local

Create a AWS user and substitute security key for values in the values.yaml. User shoiuld have s3 access rights.

  AWS_ACCESS_KEY_ID: "thekey"
  AWS_SECRET_ACCESS_KEY: "thesecret"
  
  
  values.yaml as is will create a 4 pod gateway deployment with s3 as the backend. 
  
  
 use following command after editing vaules.yaml file

# helm install --name minio-s3-gateway  -f values.yaml stable/minio




