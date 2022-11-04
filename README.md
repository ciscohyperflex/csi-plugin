#  WORK-In-Progress to keep updating this better --March 4th, 2021
# HyperFlex CSI Plugin Chart

* Installs the HyperFlex CSI Plugin to dynamically provision volumes on HyperFlex.

## TL;DR;

```console
$ helm install hxcsi \
	--set hx.url=<HX Management IP> \
	--set hx.iscsiUrl=<HX iSCSI IP> \
	--set hx.token=<HX Service Token> \
	--set hx.clientId=<HX Client-ID >
	--set hx.dockeryRegistryName=<HX dockeryRegistryName URL to pull the HXCSI images from>

Example 1: if package was extracted
helm install hxcsi --set hx.url=10.11.12.13 --set hx.iscsiUrl=10.11.12.16 --set hx.token=my_service_token --set hx.clientId=myclientId_123 --set hx.dockerRegistryName=dockerhub.xyz123.com/hx-docker ./hxcsi


Example 2: Specify the package itself
helm install hxcsi hxcsi-1.2.1.tgz  --set hx.url=10.11.12.13 --set hx.iscsiUrl=10.11.12.16 --set hx.token=my_service_token --set hx.clientId=myclientId_123 --set hx.dockerRegistryName=dockerhub.xyz123.com/hx-docker 

```

## Installing the Chart

To install the chart with the release name `my-release`:

```console
$ helm install hxcsi \
	--set hx.url=<HX Connect URL> \
	--set hx.token=<HX Connect Service Token>
```

## Uninstalling the Chart

To uninstall/delete the deployment:

```console
$ helm uninstall hxcsi 
```

## Configuration
|------------------------------|-------------------------------------------------------------|---------------------------------------------------|
| Parameter                    | Description                                                 | Default                                           |
|------------------------------|-------------------------------------------------------------|---------------------------------------------------|
| `hx.url `                    | HyperFlex Connect URL                                       | No Default Value. This is a required parameter.   |
| `hx.iscsiUrl`                | HyperFlex Connect URL                                       | No Default Value. This is a required parameter.   |
| `hx.token `                  | Service Account Token to connect to HyperFlex Connect URL   | No Default Value. This is a required parameter.   |
| `hx.clientId`                | A ClientID to isolate resouces per  Tenant                  | Optional                                          | 
| `hx.dockeryRegistryName`     | Docker hub to pull the HXCSI images from                    | Optional. Images must be on each K8s node         | 
|------------------------------|-------------------------------------------------------------|---------------------------------------------------|

Note on token: The token is assumed to have been obtained out of band of the install to be passed to the Helm install. The token need be passed AS-IS i.e.
without doing any encoding on the token received from HX Cluster.

<<<<<<< HEAD
=======
https://www.cisco.com/c/en/us/td/docs/hyperconverged_systems/HyperFlex_HX_DataPlatformSoftware/HyperFlex_Kubernetes_Administration_Guide/hxcsi-1-2/b-hx-system-admin-guide-for-kubernetes-1-2/m-configuring-hyperflex-container-storage-integration.html#Cisco_Task.dita_835e4208-873d-45c0-90db-8561113a4029


## Cisco Hyperflex CSI Operator on Red Hat OpenShift

https://catalog.redhat.com/software/operators/detail/615212f8b6d5b845070b7da0

## Cisco Hyperflex CSI Operator on Google Anthos
https://cloud.google.com/anthos/docs/resources/partner-platforms#cisco

## Cisco HyperFlex CSI Interoperability Metrics
Cisco HyperFlex CSI and Kubernetes Platform Version and Distribution Interoperability:
|HXDP Version | CSI Spec Version | Kubernetes Version |  Qualified CCP Version | Qualified Anthos Version | Qualified Open iSCSI | Qualified OpenShift Version|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 4.0(2a)|1.0|1.15|5.1, 5.2|1.3|-|-|
| 4.0(2b)|1.0|1.16| 6.0, 7.0 |1.4.1|-|-|
| 4.0(2c)|1.0|1.17|6.0, 7.0|1.5.1|-|-|
| 4.5(1a)|1.2|1.18.2|-|1.7.2|Open iSCSI - 2.0.874-5ubuntu2.10|[4.9, 4.10](https://catalog.redhat.com/software/operators/detail/615212f8b6d5b845070b7da0) |
| 4.5(2a)|1.2|1.18.2, 1.19.8|-|-|Open iSCSI - 2.0.874-5ubuntu2.10|-|
|5.0(1a)|1.2(2a)|1.19.8|-|-|Open iSCSI - 2.0.874-5ubuntu2.10|-|
|5.0(2a)|1.2(3a)|1.22.7|-|1.11|Open iSCSI - 2.0.874-5ubuntu2.10|-|

## Troubleshooting

The [document](https://www.cisco.com/c/en/us/td/docs/hyperconverged_systems/HyperFlex_HX_DataPlatformSoftware/HyperFlex_Kubernetes_Administration_Guide/hxcsi-1-2/b-hx-system-admin-guide-for-kubernetes-1-2/m-k8-troubleshooting.html)  highlights common issues seen when installing and using the HyperFlex CSI integration. The information provided includes symptoms to help diagnose the issue as well as a solution to resolve the issue.
>>>>>>> parent of bfbc150 (Update README.md)
