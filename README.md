# Qwiklab: Automating the Deployment of Infrastructure Using Deployment Manager
<p align="center"><img src="infra.png" width="700px"></p>

# Usage
## To preview deployment
```
gcloud deployment-manager deployments create dminfra --config=config.yaml --preview

> OUTPUT
NAME                               TYPE                 STATE      
mynet-eu-vm                        compute.v1.instance  IN_PREVIEW
mynet-us-vm                        compute.v1.instance  IN_PREVIEW
mynetwork                          compute.v1.network   IN_PREVIEW
mynetwork-allow-http-ssh-rdp-icmp  compute.v1.firewall  IN_PREVIEW
```
## Apply deployment
```
gcloud deployment-manager deployments update dminfra

> OUTPUT
NAME                               TYPE                 STATE      ERRORS  INTENT
mynet-eu-vm                        compute.v1.instance  COMPLETED  []
mynet-us-vm                        compute.v1.instance  COMPLETED  []
mynetwork                          compute.v1.network   COMPLETED  []
mynetwork-allow-http-ssh-rdp-icmp  compute.v1.firewall  COMPLETED  []
```
## Delete deployment
```
gcloud deployment-manager deployments delete dminfra
```
