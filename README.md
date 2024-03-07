# homelab-kube-vip

This is a mirco-services repo for deploying
[kube-vip](https://kube-vip.io)
into [my homelab](https://github.com/charlesthomas/homelab).

using `kube-vip` in ARP mode to create a virtual IP that points to any active control-plane node in the cluster via one IP

## pull kubectl config

once the .3 vip is returning pings, you can pull the `k3s` config for `kubectl` and configure it to connect through the .3 vip

```bash
scp k3s0:/etc/rancher/k3s/k3s.yaml ~/.kube/config
```

be sure to edit `~/.kube/config` and change the IP to the .3 vip

---
This repo is templated via
[homelab-template](https://github.com/charlesthomas/homelab-template)
and automatically updated via
[🤖 Templatron](https://github.com/charlesthomas/templatron).
