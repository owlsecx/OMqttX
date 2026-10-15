# 🦉 OMqttX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OMqttX** — IoT Message-Broker Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline IoT message-broker configuration & ACL auditor (Mosquitto, EMQX, HiveMQ, VerneMQ, NATS)

---

## ✨ Features

- Mosquitto auditor — listeners, per_listener_settings, include_dir, anonymous, TLS / websockets, bridges, limits
- password_file auditor — plaintext, $6$ vs $7$ PBKDF2
- ACL semantic analyser (wildcards, %u / %c misuse, $SYS, overlaps) + "can user U write topic T" simulator
- EMQX 5 emqx.conf (HOCON) — authn / authz, dashboard, cookie
- HiveMQ CE config.xml (entities refused) + allow-all extension
- VerneMQ vernemq.conf and NATS nats-server.conf auditors
- CWE + MITRE ATT&CK (Enterprise & ICS) mapping
- Score / grade, TXT / MD / JSON / CSV / SARIF exports
- Offline --root discovery, hardened templates, --demo
- Read-only; secrets are masked in every output

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMqttX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
