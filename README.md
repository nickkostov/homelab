# homelab
ArgoCD Bootstrap


## Hardware:

- Optiplex MFF 3050 i5-6500
- Rotuer Asus RT-AC86U

## Prerequisites

- Install k3s one as master node and two/three more as slaves/workers. 
  - Without traefik. 
  - Using metalib, using RT-AC86U.
- All machines must have configured DNS resolution locally.

### DNS

- My Local Domain Area is called range.local in respect to the fact that I love moutains.

> You might notice that I love them and call things after them. In example Desktop is Evereset.

#### Install MetalLB

```bash
kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.14.5/config/manifests/metallb-native.yaml
```
