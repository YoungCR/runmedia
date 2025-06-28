# Gluetun

VPN client in a thin Docker container for multiple VPN providers, written in Go, and using OpenVPN or Wireguard, DNS over TLS, with a few proxy servers built-in.

## Features

* Based on Alpine 3.20 for a small Docker image of 35.6MB
* Supports: AirVPN, Cyberghost, ExpressVPN, FastestVPN, Giganews, HideMyAss, IPVanish, IVPN, Mullvad, NordVPN, Perfect Privacy, Privado, Private Internet Access, PrivateVPN, ProtonVPN, PureVPN, SlickVPN, Surfshark, TorGuard, VPNSecure.me, VPNUnlimited, Vyprvpn, WeVPN, Windscribe servers
* Supports OpenVPN for all providers listed
* Supports Wireguard both kernelspace and userspace
** For AirVPN, FastestVPN, Ivpn, Mullvad, NordVPN, Perfect privacy, ProtonVPN, Surfshark and Windscribe
** For Cyberghost, Private Internet Access, PrivateVPN, PureVPN, Torguard, VPN Unlimited, VyprVPN and WeVPN using the custom provider. https://github.com/qdm12/gluetun-wiki/blob/main/setup/providers/custom.md
** For custom Wireguard configurations using the custom provider. https://github.com/qdm12/gluetun-wiki/blob/main/setup/providers/custom.md
** More in progress, see #134. https://github.com/qdm12/gluetun/issues/134
* DNS over TLS baked in with service provider(s) of your choice
* DNS fine blocking of malicious/ads/surveillance hostnames and IP addresses, with live update every 24 hours
* Choose the vpn network protocol, udp or tcp
* Built in firewall kill switch to allow traffic only with needed the VPN servers and LAN devices
* Built in Shadowsocks proxy server (protocol based on SOCKS5 with an encryption layer, tunnels TCP+UDP)
* Built in HTTP proxy (tunnels HTTP and HTTPS through TCP)
* Connect other containers to it. https://github.com/qdm12/gluetun-wiki/blob/main/setup/connect-a-container-to-gluetun.md
* Connect LAN devices to it. https://github.com/qdm12/gluetun-wiki/blob/main/setup/connect-a-lan-device-to-gluetun.md
* Compatible with amd64, i686 (32 bit), ARM 64 bit, ARM 32 bit v6 and v7, and even ppc64le 🎆
* Custom VPN server side port forwarding for Perfect Privacy, Private Internet Access, PrivateVPN and ProtonVPN
* Possibility of split horizon DNS by selecting multiple DNS over TLS providers
Can work as a Kubernetes sidecar container, thanks @rorph

## Setup

🎉 There are now instructions specific to each VPN provider with examples to help you get started as quickly as possible!

Go to the Wiki! https://github.com/qdm12/gluetun-wiki