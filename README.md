# Cisco HyperFlex CSI-plugin


## Overview
Cisco HyperFlex Container Storage Interface (CSI) is an out-of-tree container-based Kubernetes storage integration which is deployed and consumed through standard Kubernetes primitives such as Persistent Volume Claims and Storage Classes. 

## Features 
Cisco HyperFlex CSI supports the following features:
- Dynamic creation and deletion of volumes
- Dynamic volume attach and detach
- Block access support
- Clone volume (when source volume is from the same Datastore)
- PV support with different filesystems (Ext4, Ext3, XFS)
- Volume space statistics reporting per CSI specs
- Multi-writer support (ReadWriteMany) for Block Mode only.
- Kubernetes 1.18, 1.19 support
- Kubernetes 1.21, 1.22 support (HXCSI 1.2(3a) or later); Kubernetes 1.18, 1.19 support (HXCSI 1.2(2a) or later)
- Kubernetes Cluster multitenancy target masking using dedicated initiator group
- Support for CSI 1.2 Spec APIs
- Volume resize support for block mode volumes and ext3, ext4, and xfs filesystem volumes. (expansion)
- CSI Plug-in installation and upgrade through Helm chart
- Software Encrypted Volumes support (HXCSI 1.2(3a) or later)
- Volume Snapshots support (HXCSI 1.2(3a) or later)
- CHAP (Challenge-Handshake Authentication Protocol) enabled volumes (HXCSI 1.2(3a) or later)

## Certified Kubernetes versions
The following table details Kubernetes versions suitable for deployment of the Cisco HyperFlex CSI driver.

|Supported Kubernetes version |
|----------------------|
|Kubernetes v1.17|
|Kubernetes v1.18|
|Kubernetes v1.19|
|Kubernetes v1.20|
|Kubernetes v1.21|
|Kubernetes v1.22|

The updated Kubernetes versions are in progress to be certified.


## Cisco HyperFlex Systems Administration Guide for Kubernetes, HX-CSI Release 1.2(x)

https://www.cisco.com/c/en/us/td/docs/hyperconverged_systems/HyperFlex_HX_DataPlatformSoftware/HyperFlex_Kubernetes_Administration_Guide/hxcsi-1-2/b-hx-system-admin-guide-for-kubernetes-1-2/m-hx-storage-integration-for-kubernetes.html



## Deployment HXCSI Using Helm Utility (Recommended)

https://www.cisco.com/c/en/us/td/docs/hyperconverged_systems/HyperFlex_HX_DataPlatformSoftware/HyperFlex_Kubernetes_Administration_Guide/hxcsi-1-2/b-hx-system-admin-guide-for-kubernetes-1-2/m-configuring-hyperflex-container-storage-integration.html#Cisco_Task.dita_835e4208-873d-45c0-90db-8561113a4029


## Cisco Hyperflex CSI Operator on Red Hat OpenShift

https://catalog.redhat.com/software/operators/detail/615212f8b6d5b845070b7da0


## Cisco HyperFlex CSI Interoperability Metrics
Cisco HyperFlex CSI and Kubernetes Platform Version and Distribution Interoperability:
|HXDP Version | CSI Spec Version | Kubernetes Version | Cisco Qualified CCP Version | Cisco Qualified Anthos Version | Cisco Qualified OpenShift Version|
|:---:|:---:|:---:|:---:|:---:|:---:|
| 4.0(2a)|1.0|1.15|5.1, 5.2|1.3|4.2|
| 4.0(2b)|1.0|1.16| 6.0, 7.0 |1.4.1|-|
| 4.0(2c)|1.0|1.17|6.0, 7.0|1.5.1|-|
| 4.5(1a)|1.2|1.18.2|-|1.7.2|Open iSCSI - 2.0.874-5ubuntu2.10|
| 4.5(2a)|1.2|1.18.2, 1.19.8|-|-|Open iSCSI - 2.0.874-5ubuntu2.10|
|5.0(1a)|1.2(2a)|1.19.8|-|-|Open iSCSI - 2.0.874-5ubuntu2.10|
|5.0(2a)|1.2(3a)|1.22|-|-|Open iSCSI - 2.0.874-5ubuntu2.10|

## Troubleshooting

The [document](https://www.cisco.com/c/en/us/td/docs/hyperconverged_systems/HyperFlex_HX_DataPlatformSoftware/HyperFlex_Kubernetes_Administration_Guide/hxcsi-1-2/b-hx-system-admin-guide-for-kubernetes-1-2/m-k8-troubleshooting.html)  highlights common issues seen when installing and using the HyperFlex CSI integration. The information provided includes symptoms to help diagnose the issue as well as a solution to resolve the issue.
