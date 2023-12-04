


## Software comparison:

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

