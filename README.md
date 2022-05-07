# ansible-tutorial
Prerequisites: Kubernetes and Docker.

## Environment
The tutorial will provide you a complete development environment for Ansible. There are 4 pods:
- VSCode Pod
- RHEL 8 Pod
- CentOS 7 Pod
- Debian Bullseye Pod


The VSCode Pod has everything you need a text editor with terminal support and Ansible 2.9.

Credentials are the same for every image; `root:Docker!`


## How to start?

For ARM Systems:  `kubectl apply -f tutorial_arm.yaml`<br>
For x86 Systems:  `kubectl apply -f tutorial_x86.yaml`

To remove, just change appy to delete.

<br>


## How to connect?


| Pod         | DNS                               |
| ----------- | -----------                       |
| VSCode      | localhost:8443 (from your browser)|
| RHEL        | rhel-service (from inside VSCode)      |
| CentOS      | centos-service (from inside VSCode)    |
| Debian      | debian-service (from inside VSCode)    |


<br>

Scenario: https://medium.com/@caggri/ansible-basics-9f6c1ee3af
