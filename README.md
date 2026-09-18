# ansible-playbooks

A collection of playbooks for configuring systems of various purposes. Each playbook is tied to its own operating system, so before installing a system for a playbook, make sure they are compatible.

## Router VM

A playbook for configuring Alpine v3.24 as a network gateway. The idea came from a VMWare Workstation limitation whereby only one NAT network is supported. Thanks to this playbook, you can spin up a VM that will support a much larger number of networks.

WAN - eth0 (192.168.10.3)
LAN - eth1 (192.168.11.2)
LAN - eth2 (192.168.12.2)

The VM will forward all requests from the LANs to the WAN interface.

### Technical specifications

The playbook configures a fresh Alpine installation into a VM with:
- SSH access restricted to key-based authentication
- a configured firewall that also allows the VM to act as a router (gateway)
- a configured user with passwordless sudo
- tweaks required to run containers as an unprivileged user

### Where do I customize it for my setup?

The ./vars.yml file is intentionally kept monolithic because, in essence, there aren't that many settings to configure. A more conventional structure was deliberately sacrificed for simplicity.