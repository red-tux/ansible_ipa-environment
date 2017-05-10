# ansible_ipa-environment
Ansible scripts to install IPA/IdM, clients and replicas.
These scripts were origionally intended to be used within Ansible Tower.

The process to install is as follows:
1) Install a "root" IPA server.
2) Configure a host to be an IPA client
3) Configure a client to be an IPA replicant

The IPA role performs the steps necesary to configure IPA and to create some
top level zones which may not be automatically created.

The IPA-Client role handles the registration of a system to IPA, and requires
the ipa_join_account and ipa_join_password be set.

