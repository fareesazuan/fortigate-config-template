# FortiGate Configuration Templates

This repository contains common FortiGate configuration templates for real-world deployments. Useful for IT professionals and network engineers.

## 🔐 Available Templates

| Feature        | Folder      | Description                          |
|----------------|--------------|-------------------------------------|
| SSL VPN        | ssl-vpn/     | Config with split tunneling, DNS    |
| IPsec VPN      | ipsec-vpn/   | Site-to-site config (coming soon)   |
| Web Filtering  | web-filter/  | Block categories and URLs           |
| NAT Policy     | nat-policy/  | Port forwarding and IP translation  |

---

## 📂 Example: SSL VPN Configuration 

```bash
config vpn ssl settings
    set servercert "Fortinet_SSL"
    set tunnel-ip-pools "SSLVPN_TUNNEL_ADDR1"
    set dns-suffix "mycompany.local"
end
