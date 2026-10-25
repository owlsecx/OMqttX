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

OMqttX is an offline IoT message-broker configuration and ACL auditor for Mosquitto, EMQX, HiveMQ CE, VerneMQ, and NATS. It reviews listeners, auth, TLS, bridges, password files, and ACL semantics (including a can-user-write-topic simulator). Secrets are masked; reports include score/grade and TXT/MD/JSON/CSV/SARIF export.

---

## ✨ Features

- Mosquitto auditor: listeners, per_listener_settings, include_dir, anonymous, TLS/websockets, bridges, limits
- password_file audit (plaintext vs `$6$`/`$7$` PBKDF2) and ACL semantic analysis with wildcards / `%u` / `%c` / `$SYS`
- `--simulate USER ACTION TOPIC` ACL simulator with optional `--client-id`
- EMQX 5 HOCON, HiveMQ CE config.xml, VerneMQ, and NATS nats-server.conf auditors
- CWE + MITRE ATT&CK (Enterprise & ICS) mapping; offline `--root` discovery; hardened templates
- Score/grade, multi-format export, `--demo` and CI severity gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMqttX --mosquitto mosquitto.conf --acl aclfile --scan
./OMqttX --simulate alice write sensors/# --format json -o mqtt.json
./OMqttX --demo --fail-on high
./OMqttX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
