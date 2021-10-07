# openvpn

* chart based on [stable/openvpn](https://github.com/helm/charts/tree/master/stable/openvpn) that was deprecated 
* minimal openvpn docker image
* [ovpn-admin](https://github.com/flant/ovpn-admin) tool that is maintained by Flant

```bash
helm install openvpn ./helm --create-namespace -n openvpn
```