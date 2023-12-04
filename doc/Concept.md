# Instruments for K8S local testing

## Description:
### Minikube
Minikube was started by a Kubernetes SIG, a special interest group, that recognized the need for local Kubernetes environments. Today, the SIG is very close to the Kubernetes development team and hence up-to-speed with the official Kubernetes code base.

### KinD


### K3D

## Characteristics:
### Minikube minimum requierements for the host:
- CPU: 2
- Memory: 2GB
- Disk space: 20GB

### 


## Pros and Cons:
### Minikube Pros
- Easy to install
- Light
- Add functionality with addons

### Minikube Cons
- Too minimal
- Single node
---------------------------------
### KinD Pros
- Very easy to install
- Cluster easy to deploy

### KinD Cons
- Network external access to the cluster more complicated
---------------------------------
### K3D Pros
- Very light version of Kubernetes
- Very easy to install
- Cluster easy to deploy

### K3D Cons
- Some functionalities are missing
- Do not use Docker as the default container runtime

## Demo:



### Software comparison:

| Specs                          | Minikube                          | KinD                 | K3D                                   |
|--------------------------------|-----------------------------------|----------------------|---------------------------------------|
| Runtime                        | VM                                | Container            | Native                                |
| Supported architecture         | AMD64                             | AMD64                | AMD64, ARMv7, ARM64                   |
| Supported container runtimes   | Docker, CRI-O, containerd, gvisor | Docker               | Docker, containerd                    |
| Startup time initial/following | 5:19 / 3:15                       | 2:48 / 1:06          | 0:15 / 0:15                           |
| Memory requirements            | 2GB                               | 8GB (Windows, MacOS) | 512MB                                 |
| Requires root?                 | No                                | No                   | Yes (rootless is experimental)        |
| Multi-cluster support          | Yes                               | Yes                  | No (can be achieved using containers) |
| Multi-node support             | No                                | Yes                  | Yes                                   |

