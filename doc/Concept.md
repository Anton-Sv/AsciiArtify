# Instruments for K8S local testing

## Description:
### Minikube
Minikube is a tool for running Kubernetes clusters on a local machine. It is an open-source project and is supported by the Kubernetes community. With Minikube, you can create a single-node Kubernetes cluster that can be used for testing, development, or learning purposes.

### KinD
KinD (Kubernetes in Docker) is another tool for running Kubernetes clusters on a local machine. It uses Docker containers to simulate a Kubernetes cluster, and it can be used for testing, development, or learning purposes.

### K3D
k3d is a tool for running Kubernetes clusters on a local machine using Docker. It is designed to be lightweight and easy to use, making it a popular choice for developers who want to quickly spin up a Kubernetes cluster for testing or development purposes.

## Characteristics:
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

## Pros and Cons:
One of the primary benefits of Minikube is its ease of use. It can be installed and set up in just a few minutes, and it requires minimal configuration. Additionally, Minikube provides a built-in dashboard that allows you to view and manage your cluster from a web browser. A very important difference between minikube and all other contestants is that it can deploy Kubernetes clusters with one of the multiple drivers. A big plus for minikube is its comprehensive documentation. With minikube a developer can use practically any required Kubernetes feature. Other features are controlled by the addons system of minikube. With Minikube profiles (logical clusters that can be started and stopped separately from each other) you can create independent environments. The only downsides are single-node application, slower work and poor automation options (no config file to create whole cluster as specified). 

One of the primary benefits of KinD is its flexibility. It allows you to customize your cluster by adding or removing nodes, changing configuration settings, and installing additional software. Additionally, KinD provides a built-in dashboard that allows you to view and manage your cluster from a web browser. It is very similar to k3d with the almost identical options and limitations. 

One of the primary benefits of k3d is its speed. It can create a fully functional Kubernetes cluster in just a few seconds, and it requires minimal configuration. All you need to have is config file for your cluster. Additionally, k3d provides a built-in dashboard that allows you to view and manage your cluster from a web browser. Also it comed with traefik as an ingress controller. However, K3D does not provide so many features on the command line compared to minikube. 

## Demo:
![Image](.data/demo.gif)

## Conclusion:
When it comes to choosing between Minikube, KinD, and k3d, there is no clear winner. Each tool has its own unique features and benefits, and the best choice for you will depend on your specific needs and preferences.

If you value ease of use and a built-in dashboard, Minikube may be the best choice for you. If you need a highly customized cluster and value flexibility, KinD may be the best choice for you. If you value speed and lightweight design, k3d may be the best choice for you.

Ultimately, I will suggest firstly to try with Minikube because of its simplicity to install and use, custom addons and visual board. Because the main benefit of other tools is its speed and multi-node functionality.
