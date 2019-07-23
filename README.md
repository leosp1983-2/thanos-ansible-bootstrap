# thanos-ansible-bootstrap
Small Ansible Project / 2 Roles to bootstrap Thanos sidecars and query runners with minio s3 backend

## Please note that we are doing unencrypted traffic between the sidecars and the S3 storage. SSL Certificate can be added
## Still missing: thanos store gateway to get old data out of the minio S3 storage. Will add that soon! 

### Requirements: Please note that you have to have docker, docker-compose as well as ansible installed ###

ansible-playbook up.yml

This will spawn up 2 instances of the "Backend" Part which consists of ONE Prometheus Server with a very basic config file and ONE thanos sidecar which is connected to a cental minio S3 storage.


This will also spawn up 1 instance of the "Frontend" part which consists of ONE minio S3 storage image and ONE thanos query frontend.

