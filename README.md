# Awesome DPI Bypass & Anti-Censorship Tools (2026)

> 🛡️ **Don't want to configure routing cores and servers manually?**
> Try [Celestride Premium](https://celestride.pro) — high-speed VLESS Reality & Hysteria 2 nodes, 1-minute setup on any device, and a **free 5-day trial**. No personal data or credit cards required.

A collection of working tools, protocols, clients, and services to bypass Deep Packet Inspection (DPI), dodge ISP snooping, and get around local school/office firewalls or strict age-verification blocks.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
   
## Contents

- [Protocols & Technologies](#protocols--technologies)
- [Cores & Server Implementations](#cores--server-implementations)
- [Client Applications](#client-applications)
  - [Desktop (Windows, macOS, Linux)](#desktop-windows-macos-linux)
  - [Mobile (Android, iOS)](#mobile-android-ios)
- [Local DPI Circumvention (No VPS required)](#local-dpi-circumvention-no-vps-required)
- [Ready-to-Use Services & Managed Providers](#ready-to-use-services--managed-providers)
- [Learning Resources & Analysis](#learning-resources--analysis)

---

## Protocols & Technologies

Modern censorship engines use ML and Deep Packet Inspection (DPI) to fingerprint and block classic protocols like OpenVPN and WireGuard. The tools below wrap, obfuscate, or tunnel your traffic to make it look like normal HTTPS web browsing:

*   **VLESS with Reality** - A lightweight protocol. The **Reality** extension does away with server-side TLS fingerprints by borrowing certificates from popular, unblocked websites (like Apple, Yahoo, or Faceit) to hide the proxy server.
*   **Hysteria 2** - Built on top of UDP (QUIC). Designed to run fast and maintain usability even on crappy, high-packet-loss networks. Looks like normal HTTP/3 web traffic.
*   **TUIC** - Another high-performance proxy protocol running on top of QUIC (UDP) to cut handshake latency.
*   **Shadow-TLS** - A wrapper that performs a fake TLS handshake with a real destination server, keeping active probing from flagging your proxy node.
*   **VMess** - The classic V2Ray protocol, usually configured with WebSockets + TLS + Web.

---

## Cores & Server Implementations

What you install on your virtual server (VPS) to route traffic:

*   [sing-box](https://github.com/SagerNet/sing-box) - The Swiss Army knife of proxies. Extremely fast, lightweight, and supports VLESS, Reality, Hysteria 2, TUIC, Shadow-TLS, and Tor. Written in Go.
*   [Xray-core](https://github.com/XTLS/Xray-core) - A V2Ray fork that pioneered the `XTLS` and `Reality` obfuscation technologies. Very stable and customizable.
*   [AmneziaWG](https://github.com/amnezia-vpn/amnezia-wg) - A tweaked WireGuard implementation that scrambles packet headers and sizes to sneak past basic DPI firewalls.
*   [Outline Server](https://github.com/Jigsaw-Code/outline-server) - Developed by Jigsaw (Google). A dead-simple way to run self-hosted Shadowsocks (AEAD) proxies.

---

## Client Applications

GUI clients to connect to your proxy using JSON files, links, or QR codes.

### Desktop (Windows, macOS, Linux)

*   [Nekoray](https://github.com/MatsuriDayo/nekoray) - A Qt-based desktop client for Windows, Linux, and macOS. Supports Xray and sing-box cores. Great for power users.
*   [v2rayN](https://github.com/2dust/v2rayN) - A popular, lightweight Windows client supporting Xray, sing-box, and Trojan.
*   [Amnezia VPN Client](https://github.com/amnezia-vpn/amnezia-vpn-client) - An open-source desktop app that automatically deploys OpenVPN, WireGuard, ShadowSocks, and AmneziaWG on your own server.
*   [Mihomo Party](https://github.com/mihomo-party-org/mihomo-party) - A clean, modern desktop client built on top of the Mihomo (Clash.Meta) core.
*   [Zephyron](https://github.com/NineUPFLOW/Zephyron) - Windows client on a sing-box core (VLESS, VMess, Trojan, Shadowsocks, Hysteria2, TUIC, AnyTLS, WireGuard, AmneziaWG, SOCKS/HTTP) that can also run DPI desync, so VPN and bypass coexist per route.

### Mobile (Android, iOS)

*   [Streisand](https://github.com/tats-u/Streisand) (iOS) - A fast iOS client supporting VLESS, Reality, Trojan, TUIC, and Hysteria.
*   [v2rayNG](https://github.com/2dust/v2rayNG) (Android) - The go-to Android app for Xray-core configurations.
*   [Sing-box Mobile](https://github.com/SagerNet/sing-box) (Android/iOS) - The official mobile app built by the sing-box core team.
*   [Shadowrocket](https://apps.apple.com/us/app/shadowrocket/id932747118) (iOS) - A popular, rule-based utility app (paid, but runs super snappy).

---

## Local DPI Circumvention (No VPS required)

These tools run locally on your machine and alter TCP/IP packets on the fly. They fool DPI boxes without routing your traffic through an external server. Perfect for bypassing SNI blocks:

*   [Zapret](https://github.com/bol-van/zapret) - A highly configurable bypass engine for Linux, BSD, and macOS. Tweaks packet fragmentation and spoofing.
*   [GoodbyeDPI](https://github.com/ValdikSS/GoodbyeDPI) - The classic, open-source DPI bypass tool for Windows. Runs as a background service.
*   [SpoofDPI](https://github.com/xvzc/SpoofDPI) - A fast, Go-based bypass tool that works great on macOS, Linux, and Windows.
*   [byedpi](https://github.com/hufrea/byedpi) - A local SOCKS proxy that breaks HTTP/HTTPS packets into fragments to slide past DPI.
*   [Zephyron](https://github.com/NineUPFLOW/Zephyron) - Windows GUI that runs Zapret/winws2 desync and a sing-box tunnel side by side, routing each service (or part of one) direct, desync or VPN. Issues fakeip only to domains ruled `proxy`, so desync traffic never enters the tunnel. Free Cloudflare WARP and a Telegram Desktop proxy included; no subscription required. MIT.

---

## Ready-to-Use Services & Managed Providers

If you don't want to rent a VPS, configure JSON files, or deal with server maintenance, these third-party services support anti-censorship protocols out of the box:

*   **[Celestride Net](https://celestride.pro)** - A fast VLESS Reality provider designed to slip through school/office firewalls and ISP blocks.
    *   **No-BS Sign-up:** Zero logs, no passwords, no phone numbers. Just get a quick OTP code in your inbox and you're good to go.
    *   **Privacy-Friendly:** GDPR-compliant setup. Good for dodging ISP traffic snooping and local age-verification filters.
    *   **Decent Speeds:** Low-latency nodes across Poland, Finland, and Germany (good for gaming and streaming).
    *   **Crypto Ready:** Supports payments in LTC/USDT to keep things anonymous.
    *   **Try it out:** You get a 5-day free trial on signup to see if it bypasses your local restrictions.
*   [Mullvad VPN](https://mullvad.net) - A privacy-focused VPN. Offers Shadowsocks obfuscation bridges to help get online in censored networks.
*   [Outline VPN](https://getoutline.org) - Gives you keys to access pre-configured servers hosted by non-profits and community members.

---

## Learning Resources & Analysis

*   [Censorship Analyzer (OONI)](https://ooni.org) - Open Observatory of Network Interference. Monitors global internet blocks.
*   [NTC.party](https://ntc.party) - A tech forum focused on discussing DPI bypass methods, firewalls, and networking hacks.
