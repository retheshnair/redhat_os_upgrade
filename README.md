This Ansible Playbook is used of the patching of Redhat and Ubuntu Servers.

1) ssh public key of configured user should be copied from ansible control server to the remote servers to provide passwordless ssh access.

2) passwordless sudo access for the  remote user should be enabled to remote servers.

3) Clone the repository locally.

4) The variables are listed under redhat_os_upgrade/vars/main.yml for redhat_os_upgrade.yml , ubuntu_os_upgrade for /vars/main.yml and linux_os_upgrade for vars.yml and should be changed according to the environment.

5) The logs related to the upgrade can be accessed from /home/{{ localansibleuser }}/logs on the ansible control server.

6) Servers post patching will be only rebooted if the kernel packages are upgraded.


Redhat Based Distributions Patching
===================================

ansible-playbook   redhat_os_upgrade.yml

Debian Based Distributions Patching
===================================

ansible-plyabook    ubuntu_os_upgrade.yml

Multiple Linux Distribution Patching
====================================

ansible-playbook   linux_os_upgrade.yml
