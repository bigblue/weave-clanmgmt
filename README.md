# weave-clanmgmt
The beginnings of a weave c-lan management interface backed by etcd

```bash
USAGE: weave-clanmgmt COMMAND [OPTION]...

COMMANDS:

  create clan [clan-name]
    example: weave-clanmgmt create clan myclan

  create network [network/cidr] [clan-name]
    example: weave-clanmgmt create network 172.16.0.0/24 myclan

  destroy clan [clan-name]
    example: weave-clanmgmt destroy clan myclan

  destroy network [clan-name] [network-block]
    example: weave-clanmgmt destroy network myclan 172.16.0.0

  assign [clan-name] [hostname]
    Assign first available ip to hostname and output ip address

  detach [clan-name]
    Unassign the mapped ip for the current host and call weave hide

  status
    List clans this host is attached to
```
