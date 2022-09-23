# DevBox

DevBox is an [Ansible][1] playbook ment to provision a personal machine running [Manjaro][2].
It is inteded to run locally on a frech installation, but due to Absible's idempotent
nature it may also be run on top of an already configured machine.

## Running

First, sync mirrors and install Ansible:

	$ pacman -Syy python-passlib ansible

Second, run the playbook as root.

	# ansible-playbook -i localhost playbook.yml

When run, Ansible will prompt for the user password.

## SSH

By default, Ansible will attempt to install the private SSH key for the user.
The key should be available at the path specified in the `ssh.user_key` variable. 
Removing this variable will cause the key installation task to be skipped.


[1]: https://www.ansible.com
[2]: https://manjaro.org
