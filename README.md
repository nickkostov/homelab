# homelab
ArgoCD Bootstrap


## Hardware:

- Optiplex 3050 MFF:
  - Intel(R) Core(TM) i5-6500T CPU @ 2.50GHz
  - 8GB DDR4-SODIM
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

- Apply the configurations from metallb if you have reserved your ip ranges.
- Done.

Test with contents in test dir.

http://test-nginx.range.local

In order to trick the router, I have created a fake MAC address in order to expose the nginx service.