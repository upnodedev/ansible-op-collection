# Upnode's Optimism Ansible Collection - upnodedev.op

This collection comprises Ansible roles designed for the deployment of the Optimism full and archive nodes, as well as the OP Stack. Below is a list of the included Ansible roles:

* [roll-op-ansible](https://github.com/upnodedev/roll-op-ansible) - The simplest way to spin up your own OP Stack rollup with EIP-4337 account abstraction infrastructure using [roll-op](https://github.com/0xFableOrg/roll-op) from [0xFableOrg](https://github.com/0xFableOrg)
* More coming soon...

## How to Install

There are two ways to install Upnode's Optimism Ansible Collection (upnodedev.op) to be used in your playbook and role.

### Installing the whole collection

The most simple way is to install the whole collection with the following command.

```
ansible-galaxy collection install upnodedev.op
```

This command will install all related roles at once.

### Installing each role

In some case, you only want a specific role in the collection. You can install a specific role with the following command.

```
ansible-galaxy collection install upnodedev.op
```

For example,

```
ansible-galaxy collection install upnodedev.op
```

## Example Playbooks

### upnodedev.op.roll_op

```
- hosts: servers
  roles:
     - role: upnodedev.op.roll_op
  vars:
    roll_op_status: started
    roll_op_l1_rpc: 'https://eth-sepolia.g.alchemy.com/v2/...<ALCHEMY_API_KEY>...' 
    roll_op_seed_phrase: 'test test test test test test test test test test test junk'
```

