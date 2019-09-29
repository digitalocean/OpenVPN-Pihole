# Client Scripts

These scripts serve as examples for setting up and tearing down a Pihole +
OpenVPN server on demand.

## Scripts

*vpn-up:* Create a Pihole + OpenVPN droplet and retrieve the `client.ovpn`

*vpn-down:* Destroy all Pihole + OpenVPN droplets created by `vpn-up`

## Dependencies

- ccrypt
- jq
- openssh
- wget
