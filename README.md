# Commands to Remember

Build an Execution Environment (EE) image | ``ansible-builder build --tag test_ee``
- Make sure to be in the ee directory where execution-environment.yml lives

Run a playbook using an Execution Environment |
``ansible-navigator run test_localhost.yml --execution-environment-image base_ee --mode stdout --pull-policy missing --container-options='--user=0'``
- Make sure to be in the playbooks directory where the playbook file lives

Reminder: make this a repo for long-term access

## Podman

> Used for spinning up Ansible execution environment image

View existing EE images | ``podman images``

Remove an image | ``podman image rm <image-name>``

Remove all dangling images | ``podman image prune``
- Dangling images don't have tags or a repository name
- ``-a`` | Removes all unused images, even if they aren't dangling
- Ex: ``podman image prune -a``

Remove dangling and unused images, stopped contianers, unused volumes, and unused networks | ``podman system prune -a``

Resources:
- [Podman Commands](https://docs.podman.io/en/latest/Commands.html)
- [ChatGPT Create WP Container](https://chatgpt.com/share/6949bfe0-0038-8002-9e73-74efb43e431c)
