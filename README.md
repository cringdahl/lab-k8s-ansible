# lab-k8s-ansible

Fill out the `lab` inventory file and the `vars.yml` file, run the below ansible playbooks, and you're done.

## Order of Operations

* node_setup.yml
* kube_dependencies.yml
* kube_workers.yml
* kube_control.yml

## Lab Caveats

This is a Raspberry Pi OS environment, meaning hostname, username, and SSH key are already installed. I've got local DNS and reserved DHCP for the nodes, so no networking updates are required, Ansible or otherwise.

You'll want to run this to get your kubeconfig:

```bash
scp n1:.kube/config ~/.kube/config
```