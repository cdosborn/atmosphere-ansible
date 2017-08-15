sshkey-host-access
=========

Enable ssh access from an external host to the playbook target as user

If the host has an existing public key, it can specify a path
EXTERNAL_HOST_PUBLIC_KEY_PATH (located on the EXTERNAL_HOST), otherwise a
keypair will be created.

Role Variables
--------------

| Variable                      | Required   | Default    | Choices                       | Comments                                   |
|-------------------------------|------------|------------|-------------------------------|--------------------------------------------|
| USERNAME                      | yes        |            |                               | Username that EXTERNAL_HOST can ssh as     |
| EXTERNAL_HOST                 | yes        |            |                               | Ansible host that is granted ssh privilege |
| EXTERNAL_HOST_PUBLIC_KEY_PATH | no         |            | <path to existing public key> | Path to existing public key for access     |
| EXTERNAL_HOST_KEY_OWNER       | no         | root       |                               | Owner of generated key pair                |
| EXTERNAL_HOST_KEY_GROUP       | no         | root       |                               | Group of generated key pair                |
| EXTERNAL_HOST_KEY_DIR         | no         | /root/.ssh |                               | Location of generated key pair             |
| EXTERNAL_HOST_KEY_NAME        | no         | id_rsa     |                               | Name of generated key pair                 |

Example Playbook
----------------

See `ansible/playbooks/instance_deploy/41_shell_access.yml`

Assumption: keys generated will automatically be added as a default key

Author Information
------------------

https://cyverse.org
