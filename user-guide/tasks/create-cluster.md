# Create a Kubernetes Cluster
 
You can create any [Kubernetes cluster](https://kubernetes.io/docs/tutorials/kubernetes-basics/create-cluster/) (preferably K8s version 1.16 or higher) for installing Devtron.

You can create a cluster using one of the following cloud providers as per your requirements:

| Cloud Provider | Description |
| --- | --- |
| **AWS EKS** | Create a cluster using [AWS EKS](https://docs.aws.amazon.com/eks/latest/userguide/getting-started-console.html). <br>`Note`: You can also refer our customized documentation for installing  `Devtron with CI/CD` on AWS EKS [here](https://github.com/devtron-labs/devtron/blob/b33a37bb608d07966c8f8b89e4f59287db873c6c/docs/setup/install/install-devtron-on-aws-eks.md).</br>  |
| **Google Kubernetes Engine (GKE)** | Create a cluster using [GKE](https://cloud.google.com/kubernetes-engine/). |
| **Azure Kubernetes Service (AKS)** | Create a cluster using [AKS](https://learn.microsoft.com/en-us/azure/aks/). | 
| **k3s - Lightweight Kubernetes** | Create a cluster using [k3s - Lightweight Kubernetes](https://devtron.ai/blog/deploy-your-applications-over-k3s-lightweight-kubernetes-in-no-time/).<br>`Note`: You can also refer our customized documentation for installing `Helm Dashboard by Devtron` on `Minikube, Microk8s, K3s, Kind` [here](../../setup/install/Install-devtron-on-Minikube-Microk8s-K3s-Kind.md).</br> | 


---

## Requirements to Fulfill

The minimum requirements for installing `Helm Dashboard by Devtron` and `Devtron with CI/CD` as per the number of applications you want to manage on `Devtron` are provided below:

* For configuring small resources (to manage not more than 5 apps on Devtron):

| Integration | CPU | Memory |
| --- | :---: | :---: |
| **Devtron with CI/CD** | 2 | 6 GB |
| **Helm Dashboard by Devtron** | 1 | 1 GB |

* For configuring medium/larger resources (to manage more than 5 apps on Devtron):

| Integration | CPU | Memory |
| --- | :---: | :---: |
| **Devtron with CI/CD** | 6 | 13 GB |
| **Helm Dashboard by Devtron** | 2 | 3 GB |

> Refer to the [Override Configurations](../install/override-default-devtron-installation-configs.md) section for more information.

**Note:**
* Please make sure that the recommended resources are available on your Kubernetes cluster before you proceed with Devtron installation.
* It is NOT recommended to use brustable CPU VMs (T series in AWS, B Series in Azure and E2/N1 in GCP) for Devtron installation to experience consistency in performance.