# weave-clanmgmt
The beginnings of a weave c-lan management interface backed by etcd

```bash
USAGE: weave-clanmgmt COMMAND [OPTION]...

COMMANDS:

  create clan [clan-number] [clan-name]
    example: weave-clanmgmt create clan 9999 myvlan

  create network [network/cidr] [clan-number]
    example: weave-clanmgmt create network 172.16.0.0/24 9999

  destroy clan [clan-number]
    example: weave-clanmgmt destroy clan 9999

  destroy network [clan-number] [network-block]
    example: weave-clanmgmt destroy network 9999 172.16.0.0

  attach [clan-name]
    Assign first available ip to current host and expose through weave

  detach [clan-name]
    Unassign the mapped ip for the current host and call weave hide

  status
    List clans this host is attached to
```
