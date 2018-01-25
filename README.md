# .NET Containerization with Kubernetes, Helm, and Draft

## Technologies Covered

* [Azure Container Service v1 (ACS)](https://docs.microsoft.com/en-us/azure/container-service/kubernetes/)
* [Azure Container Service v1 (AKS)](https://docs.microsoft.com/en-us/azure/aks/)
* [Kubernetes](https://kubernetes.io)
* [Helm](https://helm.sh)
* [Draft](https://draft.sh)

This project is the demo powershell file, scripted demo and supporting files for presenting Azure Container Service (AKS) with Helm and Draft.

## Requirements

As of 1/24/2018 this demo must be run within Linux as Draft is not compatible with Windows or with Ubuntu in Windows.

## Contents

```sh
.
├── installPowershell.sh
├── .NET Containerization with K8s, Helm, and Draft.pptx
├── README.md
├── script
└── Start-Demo.ps1
```

### installPowershell.sh

Run this first to setup Powershell in your linux box. This script is designed for Ubuntu 16.04. For other versions or more information see [Powershell - Package Installation Instructions](https://github.com/PowerShell/PowerShell/blob/master/docs/installation/linux.md)

### .NET Containerization with K8s, Helm, and Draft.pptx

Slide deck for the presentation given prior to the demo.

### README.md

This file.

### script

This file is the demo script.  It is a Powershell file, but is not designed to be executed as such. Again this is designed for Ubuntu 16.04.

### Start-Demo.ps1

This file runs a provided script and allows your to execute, or skip steps via keyboard shortcuts.  Once you start the demo press '?' to display the keys.

## To run this step by step demo

```powershell
pwsh ./Start-Demo.ps1 ./script
```

## Items To Replace

Pay attention to the lines below to remove Ubuntu specific or names that may be in use by other users.

### Ubuntu 16.04 Specific Items

* Any 'apt' or 'apt-get' call.
* Install dotnet

```powershell
# Install dotnet
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-xenial-prod xenial main" > /etc/apt/sources.list.d/dotnetdev.list'
sudo apt-get update
sudo apt-get install -y apt-transport-https
sudo apt-get install -y dotnet-sdk-2.1.4
```

### MacOS Specific Items

* Anything related to 'brew' which is [homebrew](https://brew.sh/).

### Variables

* The Azure Resource Group "k8sJvB"
* The Kubernetes Clusters "JvBK8sClusterOld" and "JvBK8sCluster"
* Your path to the installed Azure 2.0 cli

```powershell
sudo /home/jvb/bin/az aks install-cli
```

### Questions or Comments

Updates to this demo will be published to [@jasonvanbrackel](https://www.twitter.com/jasonvanbrackel) on twitter and my site [morehuman.software](https://morehuman.software)