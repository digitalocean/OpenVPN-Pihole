# OpenVPN + Pihole

https://marketplace.digitalocean.com/apps/openvpn-pihole

## Setup

    python3 -m venv venv
    venv/bin/pip install -U pip
    venv/bin/pip install fabric

### Test build

    venv/bin/fab testbuild -H [BUILD_DROPLET_IP]

This will install your files and packages and run your scripts but will not
perform a cleanup of the build system or power it down.  This can be used for
testing during development.

### Final build

    venv/bin/fab build -H [BUILD_DROPLET_IP]

This task will perform all steps (upload files, run scripts, install packages,
clean up build system, power off) to prepare your droplet for snapshot.

## Development

See the [Marketplace Partners guide](https://github.com/digitalocean/marketplace-partners/tree/master/fabric)

## Common Issues

### Unsupported key file

Error:

    paramiko.ssh_exception.SSHException: not a valid RSA private key file

[Fix](https://freelancing.studio/paramiko-and-rsa-key/):

    puttygen id_rsa -O private-openssh -o new.key

## Donations

If you like this tool, consider donating to the authors from which this work
is derived:

    https://github.com/Nyr/openvpn-install#donations
    https://pi-hole.net/donate/
