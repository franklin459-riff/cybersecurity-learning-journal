# 🖥️ Environment Setup

## Objective

To build an isolated virtual lab environment for learning and practicing cybersecurity concepts without impacting production systems.

The environment is designed to evolve over time as new technologies and enterprise services are introduced.

---

# 🛠️ Lab Environment

| Component | Purpose |
|-----------|---------|
| Windows 11 | Host Operating System |
| VMware Workstation | Virtualization Platform |
| Kali Linux | Attacker Machine |
| Metasploitable 2 | Intentionally Vulnerable Target |

---

# 🌐 Network Configuration

The lab is configured using VMware virtual networking to allow communication between the virtual machines while keeping the environment isolated from production systems.

Current connectivity:

```text
Windows 11 (Host)
        │
        │ VMware Workstation
        │
 ┌──────┴────────┐
 │               │
 │               │
Kali Linux   Metasploitable 2
(Attacker)     (Target)
```

The network configuration allows:

- Communication between Kali Linux and Metasploitable 2
- Safe experimentation in an isolated environment
- Enumeration and exploitation exercises without affecting external systems

---

# 🎯 Current Capabilities

The current lab supports:

- Network discovery
- Host enumeration
- Port scanning
- Service enumeration
- Banner grabbing
- Vulnerability assessment

Additional systems and services will be added as the lab evolves.

---

# 🚀 Future Expansion

The environment will gradually be expanded to include:

- Windows Server
- Active Directory
- Windows Client
- Microsoft Entra ID
- Enterprise networking
- Security monitoring
- Endpoint protection
- Hybrid identity

---

# 💡 Key Takeaways

- VMware provides an isolated environment for safe experimentation.
- Kali Linux serves as the attack platform.
- Metasploitable 2 provides intentionally vulnerable services for learning.
- The lab is designed to grow from a simple penetration testing environment into a realistic enterprise infrastructure.