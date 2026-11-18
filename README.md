<p align="center">
  <img src="assets/banner.svg" alt="Nathan Macedo — NOC / Infraestrutura de Redes" width="100%" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2800&pause=900&color=39D353&center=true&vCenter=true&width=620&lines=%24+ping+-c+1+nathan-macedo+%E2%86%92+1+received%2C+0%25+loss;%24+traceroute+carreira%3A+suporte+%E2%86%92+NOC+%E2%86%92+infra;%24+sudo+make+homelab+--quebra-e-conserta" alt="terminal" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/nathan-emanuel-macedo/"><img src="https://img.shields.io/badge/LinkedIn-0d1117?style=for-the-badge&logo=linkedin&logoColor=00E5FF" /></a>
  <a href="mailto:nathancybersec@gmail.com"><img src="https://img.shields.io/badge/Email-0d1117?style=for-the-badge&logo=gmail&logoColor=00E5FF" /></a>
  <a href="https://github.com/NathanCyber-Sec/Home-Lab"><img src="https://img.shields.io/badge/Homelab-online-0d1117?style=for-the-badge&logo=proxmox&logoColor=39D353&labelColor=0d1117&color=1a7f37" /></a>
</p>

---

### `> show running-config | section nathan`

```cisco
hostname nathan-macedo
!
interface Carreira0/0
 description Suporte de TI (field + helpdesk) -> NOC / Infraestrutura de Redes
 ip address 10.0.0.1 255.255.255.0
 no shutdown
!
interface Formacao0/1
 description Redes de Computadores - Estacio (conclusao 07/2027)
 no shutdown
!
router foco
 network routing-switching
 network vlan-nat-dhcp
 network firewall-virtualizacao-linux
 passive-interface security   ! IDS/SIEM como diferencial, nao como destino
!
banner motd ^ Aprendo quebrando o proprio lab e documentando o conserto ^
!
end
```

### `> show ip interface brief`

```text
Interface                  Status        Protocol   Nota
Redes (VLAN/NAT/DHCP)      up            up         MikroTik + OPNsense no lab
Linux (Debian/Ubuntu)      up            up         daily driver
Virtualizacao (Proxmox)    up            up         homelab dedicado
Active Directory           up            up         no trabalho + lab
Seguranca (Suricata/Wazuh) up            up         mini-SOC v1 do lab
Routing (OSPF)             up            down       estudando agora
AWS                        admin down    down       proxima fase
Terraform                  admin down    down       depois da AWS
```

### `> show inventory`

<p>
  <img src="https://img.shields.io/badge/MikroTik-0d1117?style=for-the-badge&logo=mikrotik&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/OPNsense-0d1117?style=for-the-badge&logo=opnsense&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/pfSense-0d1117?style=for-the-badge&logo=pfsense&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/Proxmox-0d1117?style=for-the-badge&logo=proxmox&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/Debian-0d1117?style=for-the-badge&logo=debian&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/Ubuntu-0d1117?style=for-the-badge&logo=ubuntu&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/Docker-0d1117?style=for-the-badge&logo=docker&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/Tailscale-0d1117?style=for-the-badge&logo=tailscale&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/Wireshark-0d1117?style=for-the-badge&logo=wireshark&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/Bash-0d1117?style=for-the-badge&logo=gnubash&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/Python-0d1117?style=for-the-badge&logo=python&logoColor=00E5FF" />
  <img src="https://img.shields.io/badge/Wazuh-0d1117?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Suricata-0d1117?style=for-the-badge" />
</p>

### `> show license`

<p>
  <img src="https://img.shields.io/badge/Cisco-Networking_%26_Cybersecurity_Jr-0d1117?style=flat-square&logo=cisco&logoColor=00E5FF&labelColor=0d1117&color=1f6feb" />
  <img src="https://img.shields.io/badge/Fortinet-NSE_1_%2F_2-0d1117?style=flat-square&logo=fortinet&logoColor=00E5FF&labelColor=0d1117&color=1f6feb" />
  <img src="https://img.shields.io/badge/Google-Cybersecurity_Professional-0d1117?style=flat-square&logo=google&logoColor=00E5FF&labelColor=0d1117&color=1f6feb" />
  <img src="https://img.shields.io/badge/COFPS-Hack_%26_Fix-0d1117?style=flat-square&labelColor=0d1117&color=1f6feb" />
</p>

### `> show ip route projetos`

| Code | Projeto | O que é |
|---|---|---|
| `L` lab | **[Home-Lab](https://github.com/NathanCyber-Sec/Home-Lab)** | Homelab de infra: Proxmox, OPNsense, MikroTik com VLANs e AD, com os erros e consertos documentados |
| `C` produção | **[MeuTecnico](https://github.com/NathanCyber-Sec/MeuTecnico)** | Site em produção de uma assistência técnica: [omeutecnico.com.br](https://omeutecnico.com.br/) |

### `> traceroute carreira`

```mermaid
flowchart LR
    A["Suporte de TI<br/>(hoje)"] --> B["Redes + Linux<br/>até jan/2027"]
    B --> C["AWS SAA<br/>até jun/2027"]
    C --> D["Terraform +<br/>portfólio"]
    D --> E(("NOC / Infra"))
    style A fill:#0d1117,stroke:#39d353,color:#e6edf3
    style B fill:#0d1117,stroke:#00e5ff,color:#e6edf3
    style C fill:#0d1117,stroke:#1f6feb,color:#e6edf3
    style D fill:#0d1117,stroke:#1f6feb,color:#e6edf3
    style E fill:#0d1117,stroke:#ff3b6b,color:#e6edf3
```

---

<p align="center">
  <code>! "Se não está documentado, não aconteceu." 🐧</code>
</p>
