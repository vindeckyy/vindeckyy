# Hayden

Security research and tooling. Mostly offensive-side: the scripts I reach for during engagements, detection rules tuned against my own homelab, Active Directory attack labs, and writeups for boxes I cleared. Non-security work (Linux graphics, streaming, container engines) lives in the other repos.

## What I work on

**Log4j attack surface** — three public disclosures: record corruption and log injection in Log4j, plus two RCE paths that don't require the original `log4shell` gadget.

**Router and IoT firmware** — authenticated OS command injection in the TP-Link Archer AXE300 speed-test daemon (CWE-78, CVSS 8.5), and unauthenticated LAN JS execution with persistent internal-API control on VIZIO/OS SmartCast TVs.

**Detection engineering** — Sigma, Suricata and Zeek rules plus KQL/SPL hunts, written against real traffic from a lab I run (Proxmox host, Windows servers, a DC, a Linux jump box). Every rule ships with the match it was written against; false positives are logged per rule.

**AD tradecraft** — labs for kerberoasting, AS-REP roasting, NTLM relay and coercion, delegation abuse, BloodHound ACL paths, and ADCS ESC1–8. Each lab has a reproduce-from-clean script against a throwaway DC.

## Repos

| Repo | Contents |
| --- | --- |
| [pentest-toolbox](https://github.com/vindeckyy/pentest-toolbox) | Recon, web, exploit and post-ex scripts, wordlists, engagement notes |
| [ctf-writeups](https://github.com/vindeckyy/ctf-writeups) | HackTheBox, TryHackMe and event CTF writeups — recon to root |
| [homelab-detection-lab](https://github.com/vindeckyy/homelab-detection-lab) | Sigma/Suricata/Zeek rules and SIEM queries with FP notes |
| [ad-attack-lab](https://github.com/vindeckyy/ad-attack-lab) | AD attack labs with reproduce scripts |
| [log4j-log-injection](https://github.com/vindeckyy/log4j-log-injection) | Log injection and record corruption in Apache Log4j |
| [log4j-classpath-plant-rce](https://github.com/vindeckyy/log4j-classpath-plant-rce) | RCE via classpath resources Log4j trusts implicitly |
| [log4j-config-time-lookup-rce](https://github.com/vindeckyy/log4j-config-time-lookup-rce) | RCE via configuration-time evaluation of Thread Context Map data |
| [tp-link-archer-axe300-command-injection-rce](https://github.com/vindeckyy/tp-link-archer-axe300-command-injection-rce) | Authenticated command injection in the AXE300 speed-test server |
| [smartcast-backdoor](https://github.com/vindeckyy/smartcast-backdoor) | Unauthenticated LAN JS execution on VIZIO SmartCast TVs |

Elsewhere: [OpenBoxGL](https://github.com/vindeckyy/OpenBoxGL) (OpenGL-first game library and launcher), [lumen](https://github.com/vindeckyy/lumen) (LAN remote desktop in Rust), [ingot-engine](https://github.com/vindeckyy/ingot-engine) (container engine from scratch in Rust), [fan-control](https://github.com/vindeckyy/fan-control), [slipstream](https://github.com/vindeckyy/slipstream), [CastMirror](https://github.com/vindeckyy/CastMirror).

## Method

Reproduce everything yourself first — build the lab, break it, write the detection, then write it up. Findings that affect third parties get a disclosure timeline and a coordinated report rather than a public PoC drop.

Tools I live in: Nmap, Burp, Impacket, BloodHound, Rubeus, Responder, mitm6, Suricata, Zeek, Splunk, and a lot of Python.
