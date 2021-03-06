# Network and DB clusters [!KEYREF mrd-short-name]

When creating a cluster, you can:

- Set the network for the cluster itself.
- Set the subnets for each host in the cluster.

You can create a cluster without specifying any subnets for the hosts, if the availability zone selected for each host contains exactly one subnet of the cluster network.

## Network access to a cluster [!KEYREF mrd-short-name]

You can connect to a [!KEYREF RD] cluster only from a Yandex.Cloud virtual machine instance that is connected to the same network as the cluster. You cannot get a public IP address for a host in this type of cluster.

## Hostname and FQDN {#hostname}

[!KEYREF mrd-short-name] generates the name of each cluster host when it is being created. This name will be the host's fully qualified domain name (FQDN). You can use the FQDN to access the host within a single cloud network.

The hostname and, consequently, the FQDN cannot be changed.

