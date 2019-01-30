# ansible-zookeeper-ubuntu

# Description

**ansible-zookeeper-ubuntu** is a simple [Ansible](https://www.ansible.com/) role for installing [Zookeeper](https://zookeeper.apache.org/) on an Ubuntu machine.

# Usage

Define an inventory file containing a `cluster` group for clustered deployments:

```
# Stand-alone node
node

# Clustered nodes
# WARNING: make sure to define the ZooKeeper node ID (zkId)
[cluster]
node01 zkId=1
node02 zkId=2
node03 zkId=3
```

Then from the parent directory:

```
ansible-playbook -i <inventory.ini> -u root ansible-zookeeper-ubuntu/playbook.yml
```

# Contributing

[Spatial Current, Inc.](https://spatialcurrent.io) is currently accepting pull requests for this repository.  We'd love to have your contributions!  Please see [Contributing.md](https://github.com/spatialcurrent/ansible-zookeeper-ubuntu/blob/master/CONTRIBUTING.md) for how to get started.

# License

This work is distributed under the **MIT License**.  See **LICENSE** file.
