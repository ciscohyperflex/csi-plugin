# HyperFlex CSI-plugin

This repository contains  Cisco HyperFlex CSI driver deployment yamls for different OS
and kubernetes distributions. 
The repository also contains example usage for the CSI driver.

## Certified Kubernetes versions
The following table details Kubernetes versions suitable for deployment of the Cisco HyperFlex CSI driver.

|Supported Kubernetes version |
|----------------------|
|Kubernetes v1.17|
|Kubernetes v1.18|

The updated Kubernetes versions are in progress to be certified.


## Cisco HyperFlex Systems Administration Guide for Kubernetes, HXCSI Release 1.2(x)
https://www.cisco.com/c/en/us/td/docs/hyperconverged_systems/HyperFlex_HX_DataPlatformSoftware/HyperFlex_Kubernetes_Administration_Guide/hxcsi-1-2/b-hx-system-admin-guide-for-kubernetes-1-2/m-hx-storage-integration-for-kubernetes.html

Cisco HyperFlex Container Storage Interface (CSI) is an out-of-tree container-based Kubernetes storage integration; which is deployed and consumed through standard Kubernetes primitives such as Persistent Volume Claims and Storage Classes. 


## HyperFlex 4.5 Container Storage Interface (HX-CSI) Installation

https://iamjoost.com/2021/03/13/hyperflex-4-5-container-storage-interface-hx-csi-installation/


## Configuring the Cisco HyperFlex CSI Integration for Kubernetes
https://www.cisco.com/c/en/us/td/docs/hyperconverged_systems/HyperFlex_HX_DataPlatformSoftware/HyperFlex_Kubernetes_Administration_Guide/4_0/b_Cisco_HyperFlex_Systems_Administration_Guide_for_Kubernetes_4_0/b_Cisco_HyperFlex_Systems_Administration_Guide_for_Kubernetes_4_0_chapter_010.pdf

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

