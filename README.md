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

  release [clan-name] [hostname]
    Remove assigned ip for hostname and make available again

  status 
    List clans this host is attached to
```

### Managing docker container ips on a weave network

```bash
weave-clanmgmt create clan myclan
weave-clanmgmt create network 10.0.2.0 myclan
CONTAINER_IP=$(weave-clanmgmt assign myclan bb1)
weave run $CONTAINER_IP/24 -t -i --name bb1 -h bb1 busybox
```
