# Infrastruktura

Přehled toho, co v síti běží. Podrobnosti jsou na podstránkách.

```mermaid
flowchart TB
    NET[(Místní síť / repeater)] --- PVE
    subgraph PVE[Fyzický server – Proxmox]
        OPN[OPNsense<br/>router / firewall]
        AD[Windows Server<br/>Active Directory]
        DEB[Debian<br/>aplikační server]
    end
    OPN --- LAN1[LAN posádka]
    OPN --- LAN2[LAN EMMC]
```

| Stroj | Role | Adresa | Stránka |
|---|---|---|---|
| Proxmox | hypervisor | TODO | [Proxmox](proxmox.md) |
| OPNsense | router, firewall, DHCP? | TODO | [OPNsense](opnsense.md) |
| Windows Server | Active Directory, DNS? | TODO | [AD](ad-server.md) |
| Debian | aplikace | TODO | [Debian](debian-app.md) |
