Based on stable/openvpn chart (so just minimal openvpn docker image) and installed additional ovpn-admin tool that is maintained by Flant


helm install wzvpn ./helm --create-namespace -n openvpn

TODO: 
 - move to own openvpn image
 - move to own openvpn-admin image