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

