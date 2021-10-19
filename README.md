# openvpn-k8s

* chart is based on [stable/openvpn](https://github.com/helm/charts/tree/master/stable/openvpn) that was deprecated. It should help to smoothly migrate from stable/openvpn by changing chart repo
* minimal openvpn docker image that similar to original, but with updated components
* [ovpn-admin](https://github.com/flant/ovpn-admin) tool that is maintained by [Flant](https://github.com/flant). 

```bash
# install
helm install stable stable/openvpn --create-namespace -n openvpn

# ✗ helm list -A
# NAME  	NAMESPACE	REVISION	UPDATED                              	STATUS  	CHART        	APP VERSION
# stable	openvpn  	1       	2021-10-19 22:22:17.867829 +0300 EEST	deployed	openvpn-4.2.5	1.1.0
# ...
# bash-4.3# cat /etc/openvpn/certs/pki/index.txt
# V	311017193619Z		01	unknown	/CN=server
# V	311017194005Z		02	unknown	/CN=wzooff

# update
helm upgrade stable ./helm -n openvpn

# ✗ helm list -A
# NAME  	NAMESPACE	REVISION	UPDATED                              	STATUS  	CHART        	APP VERSION
# stable	openvpn  	2       	2021-10-19 22:42:03.477331 +0300 EEST	deployed	openvpn-4.3.0	2.5.2
# ...
# cat /etc/openvpn/certs/pki/index.txt
# V	311017193619Z		01	unknown	/CN=server
# V	311017194005Z		02	unknown	/CN=wzooff
```