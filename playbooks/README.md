This repository now uses the Varilink [Tools - Ansible](https://github.com/varilink/tools_ansible) tool as its playbook runner. This tool is setup to be used in conjunction with the playbooks in the Varilink [Libraries - Ansible Playbooks](https://github.com/varilink/libraries_ansible-playbooks) repository. In order to do this, the tool is configured to expect that library of playbooks is installed as a submodule at the path `playbooks/`.

The project playbooks in the [Libraries - Ansible Playbooks](https://github.com/varilink/libraries_ansible-playbooks) cater to WordPress websites. However, the DATA website is not based on WordPress and so doesn't make use of any of playbooks in that library. Instead it uses project specific playbooks that are within the root directory of this repository. Thus this `playbooks/` directory exists solely to honour the volume mapping in the `docker-compose.yml` file within [Tools - Ansible](https://github.com/varilink/tools_ansible) and contains no playbooks.

It's possible that going forwards this might change and we might instead either:

- Find that there is a use for playbooks in [Libraries - Ansible Playbooks](https://github.com/varilink/libraries_ansible-playbooks) in this project and replace this directory with that repository added as a Git submodule at the same path.

- Conclude that we're never go to find a use for playbooks in [Libraries - Ansible Playbooks](https://github.com/varilink/libraries_ansible-playbooks) in this project and possibly move this project's own playbooks into this directory.
