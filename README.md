# Threat Hunting with Splunk & MITRE ATT&CK

> Proactive threat hunting on Windows Sysmon logs using Splunk SIEM deployed on Kali Linux, focused on detecting credential dumping and remote system discovery attacks.

---

## Objective

This lab simulates a real-world post-exploitation scenario where an attacker has compromised a Windows machine and attempts to steal credentials via LSASS memory dumping.

The goal is to transition from **reactive log analysis** to **proactive threat hunting** by using Splunk to identify the digital fingerprints left behind by the attacker.

**MITRE ATT&CK Techniques Investigated:**
| Technique ID | Name | Description |
|---|---|---|
| T1003.001 | OS Credential Dumping: LSASS Memory | Attacker dumps LSASS process memory to extract plaintext credentials |
| T1018 | Remote System Discovery | Attacker enumerates other systems on the network |

---

## 🛠️ Environment Setup

| Component | Details |
|---|---|
| **SIEM Platform** | Splunk (deployed via Docker) |
| **Analyst OS** | Kali Linux |
| **Log Source** | Windows Sysmon (`windows-sysmon.log`) |
| **Log Format** | Windows Event Logs (XML) |
| **Deployment** | Containerised Splunk instance via one-click shell script |

## 📚 References

- [MITRE ATT&CK T1003.001 — LSASS Memory](https://attack.mitre.org/techniques/T1003/001/)
- [MITRE ATT&CK T1018 — Remote System Discovery](https://attack.mitre.org/techniques/T1018/)
- [Sysmon Event ID Reference](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- [Splunk Attack Dataset](https://github.com/splunk/attack_data/tree/master/datasets/attack_techniques)

---

## 👤 Author

**Shannon Tan**
