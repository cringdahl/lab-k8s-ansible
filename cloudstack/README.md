# cloudstack

Putting Rohit Yadav's [cloudstack walkthrough](https://rohityadav.cloud/blog/cloudstack-arm64-kvm/) into Ansible.

After node_setup.yml in the main, run these:

## design
The design, such as it is, is simply n1 as management server, with the workers running compute. You'll need to authenticate to each via SSH, which is enabled by Ansible adding n1's Cloudstack SSH key to root's authorized_keys file.

## control
- cs_network.yml
- cs_mgmt.yml
- cs_storage.yml

## workers
- cs_network.yml
- cs_compute.yml

