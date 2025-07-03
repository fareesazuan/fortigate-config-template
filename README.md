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


## 📂 Example: IPsec Site-to-Site VPN Configuration

This template configures a basic IKEv2 site-to-site VPN between two FortiGate firewalls.

```bash
config vpn ipsec phase1-interface
    edit "BranchTunnel"
        set remote-gw 203.0.113.1
        set psksecret yourPreSharedKey

🖼️ Diagram: ipsec-vpn/ipsec-topology.png
📄 Full config: ipsec-vpn/config.txt
