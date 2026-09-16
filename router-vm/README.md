# Why?

This playbook configures a fresh Alpine installation into a VM with:
- SSH access restricted to key-based authentication
- a configured firewall that also allows the VM to act as a router (gateway)
- a configured user with passwordless sudo
- tweaks required to run containers as an unprivileged user

# Where do I customize it for my setup?

The ./vars.yml file is intentionally kept monolithic because, in essence, there aren't that many settings to configure. A more conventional structure was deliberately sacrificed for simplicity.
