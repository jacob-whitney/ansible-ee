# Commands to Remember

Build an Execution Environment (EE) image | ``ansible-builder build --tag test_ee``
- Make sure to be in the ee directory where execution-environment.yml lives

Run a playbook using an Execution Environment |
``ansible-navigator run test_localhost.yml --execution-environment-image base_ee --mode stdout --pull-policy missing --container-options='--user=0'``
- Make sure to be in the playbooks directory where the playbook file lives

Reminder: make this a repo for long-term access

## Podman

> Used for spinning up Ansible execution environment image

View existing EE images | ``podman images list``

Remove an image | ``podman image rm <image-name>``

Resources:
- [Podman Commands](https://docs.podman.io/en/latest/Commands.html)
