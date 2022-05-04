# ansible-tutorial
Prerequisites: Kubernetes and Docker.

## Environment
The tutorial will provide you a complete development environment for Ansible. There are 4 pods:
- VSCode Pod
- RHEL 8 Pod
- CentOS 7 Pod
- Debian Bullseye Pod

<small> The total size of images: 1573MB</small>


The VSCode Pod has everything you need a text editor with terminal support and Ansible 2.9.

Credentials are the same for every image; `root:Docker!`


## How to start?

Just type:  `kubectl -f tutorial.yaml`

<br>


## How to connect?


| Pod         | DNS                               |
| ----------- | -----------                       |
| VSCode      | localhost:8443 (from your browser)|
| RHEL        | rhel-service (from inside VSCode)      |
| CentOS      | centos-service (from inside VSCode)    |
| Debian      | debian-service (from inside VSCode)    |




<br>

> The images used in this tutorial are created on an ARM-based macOS environment. If you want to create your own images you can use Dockerfiles in the repo.

<br>

Scenario will be added soon.
