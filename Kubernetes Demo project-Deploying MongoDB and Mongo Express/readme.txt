Steps for complete application setup with kubernetes components:

1) create mongodb pod
2) create internal service to interact with the pod
3) create mongo express deployment, connect using DB URL which is in ConfigMap file and username & password credentials in Secret file. Pass these through env. vars
in deployment.yaml file (reference).
4) create external service for allowing external request to talk to the pod

Browser Request Flowthrough the K8s components:

Browser -->mongo express external service --> mongo express pod --> mongodb internal service (ConfigMap:DBURL & authenticate using uname and pswd in Secret)-->mongodb pod
