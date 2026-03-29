# Best Cybersecurity Lab Tools (Defensive & Educational)

A curated list of **defensive, educational, and general-purpose cybersecurity lab tools** for learning, monitoring, troubleshooting, and authorized security testing — Switzerland-friendly, with buy links from Digitec/Galaxus and Digi-Key/Mouser.

---

## Scope & Ethics (Read First)

- **Authorization**: Use these tools only on systems and networks you **own** or for which you have **explicit, written permission**.
- **Focus**: Defense, visibility, training, hardware debugging, and diagnostics — not covert implants, credential theft, or exploitation.
- **Legal**: Comply with all applicable laws. In Switzerland, the Computer Crimes section of the Swiss Criminal Code (Art. 143/143bis StGB) prohibits unauthorized access.
- **Purpose of this list**: Help defenders, students, and homelabbers understand their own environment and build practical skills.

---

## Table of Contents

- [Account & Identity Security](#account--identity-security)
- [Network Visibility & Defense](#network-visibility--defense)
- [Endpoint Visibility](#endpoint-visibility)
- [Hardware / Embedded Debugging](#hardware--embedded-debugging)
- [RF / Spectrum Learning (Receive)](#rf--spectrum-learning-receive)
- [Home Lab Building Blocks](#home-lab-building-blocks)
- [Not Recommended / Out of Scope](#not-recommended--out-of-scope)
- [Buying Notes (Switzerland)](#buying-notes-switzerland)
- [Contributing](#contributing)

---

## Account & Identity Security

Protect your accounts with hardware-backed, phishing-resistant authentication.

| Tool | What it's for | Buy (CH / EU) |
|---|---|---|
| **YubiKey 5 NFC** (USB-A + NFC) | FIDO2/WebAuthn passkey and MFA for laptops and Android/iOS (tap NFC). Phishing-resistant. | [Digitec](https://www.digitec.ch/en/s1/product/yubico-yubikey-5-nfc-notebook-security-10233715) |
| **YubiKey 5C NFC** (USB-C + NFC) | Same as above, USB-C connector for modern laptops and phones. | [Digitec](https://www.digitec.ch/en/s1/product/yubico-yubikey-5c-nfc-notebook-security-12609449) |
| **YubiKey 5Ci** (USB-C + Lightning) | Dual-connector key for iOS Lightning devices + USB-C. | [Digitec](https://www.digitec.ch/en/s1/product/yubico-yubikey-5ci-notebook-security-12609443) |
| **SoloKey v2** | Open-source FIDO2/WebAuthn key — auditable firmware. | [Galaxus](https://www.galaxus.ch/en/s1/search?q=solokey) |

---

## Network Visibility & Defense

Tools for understanding, monitoring, and securing your own networks.

### Hardware

| Tool | What it's for | Buy (CH / EU) |
|---|---|---|
| **Managed switch with port mirroring (SPAN)** | Mirror traffic from any port to a sensor/IDS without disrupting production traffic. Example: TP-Link TL-SG108E. | [Digitec – TP-Link TL-SG108E](https://www.digitec.ch/en/s1/product/tp-link-tl-sg108e-8-ports-network-switch-6293483) |
| **Passive network TAP** | Reliable, non-injecting inline packet capture for troubleshooting and incident response. | [Mouser – Dualcomm ETAP-2003](https://www.mouser.ch/c/?q=network+tap) |
| **Mini PC / small server** (e.g., Intel NUC, Beelink) | Run OPNsense/pfSense firewall, Suricata/Zeek IDS, Syslog, and lab services on a dedicated device. | [Digitec – Mini PCs](https://www.digitec.ch/en/s1/producttype/mini-pc-barbone-164) |
| **USB isolator** | Protects your analysis host when connecting unknown or potentially malicious USB devices. | [Digi-Key – ADUM3160BRWZ](https://www.digikey.ch/en/products/detail/analog-devices-inc/ADUM3160BRWZ-RL/2310149) |

### Software

| Tool | What it's for | Link |
|---|---|---|
| **Wireshark** | Packet capture and deep protocol analysis for troubleshooting and incident response. | [wireshark.org](https://www.wireshark.org/) |
| **Nmap** | Asset inventory, port scanning, and exposure checking on authorized networks. | [nmap.org](https://nmap.org/) |
| **Suricata** | High-performance network IDS/IPS/NSM for signature-based threat detection. | [suricata.io](https://suricata.io/) |
| **Zeek** | Network security monitoring — extracts rich metadata and protocol logs for detection and investigation. | [zeek.org](https://zeek.org/) |
| **OpenVAS / Greenbone CE** | Vulnerability scanning for your own assets — identifies exposed services and misconfigurations. | [greenbone.net](https://www.greenbone.net/en/community-edition/) |

---

## Endpoint Visibility

Gain visibility into what is running on your machines.

| Tool | What it's for | Link |
|---|---|---|
| **osquery** | SQL-based endpoint inventory, configuration auditing, and detection hunting across Linux/macOS/Windows. | [osquery.io](https://www.osquery.io/) |
| **Sysmon** (Windows) | Rich Windows event telemetry (process creation, network connections, file changes) for detections and investigations. | [Microsoft Sysinternals](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon) |
| **Wazuh** | Open-source SIEM/XDR — aggregates Sysmon/auditd events, applies detection rules, and alerts. | [wazuh.com](https://wazuh.com/) |

---

## Hardware / Embedded Debugging

Diagnose and debug your own hardware, firmware, and embedded devices safely.

| Tool | What it's for | Buy (CH / EU) |
|---|---|---|
| **USB-to-UART / TTL adapter** (3.3 V / 5 V) | Serial console access for debugging, recovery, and diagnostics on your own embedded devices. | [Digi-Key – CP2102 module](https://www.digikey.ch/en/products/detail/silicon-labs/CP2102-GMR/2051614) |
| **Logic analyzer** (8-ch, 24 MHz+) | Capture and decode SPI/I²C/UART/CAN signals to understand device behavior and debug firmware. Example: Saleae Logic clone / DSLogic. | [Digitec – logic analyzers](https://www.digitec.ch/en/s1/search?q=logic+analyzer) |
| **Digital multimeter** | Voltage, current, continuity, and component checks — fundamental electrical troubleshooting. | [Digitec – multimeters](https://www.digitec.ch/en/s1/producttype/multimeter-116) |
| **Bench power supply** (adjustable, 0–30 V / 0–5 A) | Stable, current-limited power for boards and test circuits — prevents damage from voltage spikes. | [Digitec – bench power supplies](https://www.digitec.ch/en/s1/search?q=bench+power+supply) |
| **USB power meter** (voltage + current) | Check USB power draw and detect anomalies on USB peripherals. | [Digitec – USB testers](https://www.digitec.ch/en/s1/search?q=usb+power+meter) |
| **JTAG/SWD debugger** (e.g., ST-LINK V2, J-Link EDU) | Firmware debugging and development on your own microcontrollers. | [Digi-Key – ST-LINK V2](https://www.digikey.ch/en/products/detail/stmicroelectronics/ST-LINK-V2/2214535) |
| **ESD wrist strap + mat** | Prevent electrostatic damage to sensitive components while assembling or debugging boards. | [Digitec – ESD accessories](https://www.digitec.ch/en/s1/search?q=esd+wrist+strap) |
| **Soldering iron** (temperature-controlled) | Repair PCBs, attach headers, and prototype connections for legitimate device work. | [Digitec – soldering stations](https://www.digitec.ch/en/s1/search?q=soldering+station) |
| **Breadboard + jumper wire kit** | Rapid prototyping and connecting to UART/I²C/SPI headers without soldering. | [Digi-Key – breadboard kit](https://www.digikey.ch/en/products/filter/jumper-wire/640) |
| **Malicious USB Cable Detector** (O.MG Detector) | Detect hidden implants in USB cables before connecting them to your equipment. | [O.MG Official Store](https://o.mg.lol/products/omg-detector) |

---

## RF / Spectrum Learning (Receive)

Observe and learn about radio frequencies in a lawful, receive-only mode. Transmitting on regulated frequencies without a license is illegal in Switzerland (BAKOM).

| Tool | What it's for | Buy (CH / EU) |
|---|---|---|
| **RTL-SDR Blog V4** (receive-only dongle) | Low-cost SDR receiver for spectrum observation, ADS-B aircraft tracking, weather satellites, and RF education. | [RTL-SDR Store](https://www.rtl-sdr.com/store/) |
| **Wideband antenna kit** (SMA, telescopic/dipole) | Improved reception across HF/VHF/UHF bands for the RTL-SDR. | [Digi-Key – antenna accessories](https://www.digikey.ch/en/products/filter/antennas/823) |
| **SMA adapter set** | Connect different antenna types and cable formats to your SDR. | [Mouser – SMA adapters](https://www.mouser.ch/c/connectors/coaxial-connectors/?series=SMA) |

### Software

| Tool | What it's for | Link |
|---|---|---|
| **GQRX** | SDR receiver GUI — quick spectrum exploration and audio demodulation; ideal for beginners with RTL-SDR. | [gqrx.dk](https://gqrx.dk/) |
| **GNU Radio** | Powerful SDR/DSP framework for RF education, signal analysis, and protocol research (receive-mode labs). | [gnuradio.org](https://www.gnuradio.org/) |
| **SDR#** (SDRSharp) | Windows-based SDR receiver application; popular for quick spectrum scans. | [airspy.com/download](https://airspy.com/download/) |

---

## Home Lab Building Blocks

Infrastructure to build a realistic, segmented security lab at home.

| Tool | What it's for | Buy (CH / EU) |
|---|---|---|
| **Dedicated firewall appliance** (e.g., Protectli Vault, PC Engines APU) | Run OPNsense or pfSense for firewall, VPN, VLAN segmentation, and logging at your lab boundary. | [Digitec – firewall appliances](https://www.digitec.ch/en/s1/search?q=protectli) |
| **Wi-Fi AP with VLAN support** (e.g., TP-Link EAP series, Ubiquiti UniFi) | Separate guest / IoT / lab wireless networks with proper segmentation. | [Digitec – access points](https://www.digitec.ch/en/s1/producttype/access-point-wireless-548) |
| **Raspberry Pi 4 / 5** | Versatile lab node: DNS sinkhole (Pi-hole), lightweight monitoring, test services, or VPN gateway. | [Digitec – Raspberry Pi](https://www.digitec.ch/en/s1/search?q=raspberry+pi+4) |
| **External SSD** (USB 3.x, encrypted) | Store VM images, packet captures, forensic images, and backups; use with full-disk encryption (VeraCrypt/LUKS). | [Digitec – external SSDs](https://www.digitec.ch/en/s1/producttype/external-hard-disk-ssd-193) |
| **USB hub** (powered, 7-port) | Reliable power and port expansion when running multiple USB devices or lab peripherals. | [Digitec – USB hubs](https://www.digitec.ch/en/s1/producttype/usb-hub-335) |
| **Patch panel + cable kit** | Organized, labeled Ethernet connections make your lab easier to reconfigure and document. | [Digitec – patch panels](https://www.digitec.ch/en/s1/search?q=patch+panel) |

---

## Not Recommended / Out of Scope

The following **categories** are intentionally excluded from this list. They are primarily designed for unauthorized access, covert surveillance, or credential theft, and their inclusion would be contrary to the defensive focus of this repository.

| Category | Why excluded |
|---|---|
| **HID injection devices** (e.g., keystroke-injection "ducky" dongles) | Simulate keyboard input to execute arbitrary commands on unlocked computers — covert attack vector. |
| **Covert implants** (inline hardware taps disguised as accessories) | Designed to be installed secretly; intended for persistent unauthorized access. |
| **Rogue AP / Evil Portal kits** | Tools whose primary function is impersonating legitimate networks to intercept credentials. |
| **Credential harvesting / poisoning frameworks** | Designed to capture hashed or cleartext credentials from network traffic without authorization. |
| **C2 (Command & Control) frameworks** | Infrastructure for maintaining unauthorized persistent access and remote control of compromised systems. |
| **Password cracking accelerators** (GPU/wordlist attack pipelines) | Optimized for breaking authentication controls; legitimate uses are narrow and specialized. |
| **RF transmit-capable SDR setups described offensively** | Transmitting on licensed bands without authorization is illegal in Switzerland (BAKOM Art. 30 FMG). |
| **RFID/NFC cloning tools used on cards you don't own** | Cloning access credentials without permission is unauthorized access under Swiss law. |

> If you are conducting a **professional penetration test** with a signed Statement of Work, you will find more specialized tooling in purpose-built resources outside the scope of this list.

---

## Buying Notes (Switzerland)

- **Digitec / Galaxus** — Best Swiss online retailer for consumer electronics, networking gear, Raspberry Pi, and security keys. Ships from Switzerland; no customs surprises. [digitec.ch](https://www.digitec.ch) / [galaxus.ch](https://www.galaxus.ch)
- **Digi-Key** — Ships components (ICs, adapters, sensors, connectors) to Switzerland with DHL; competitive pricing for low-volume orders. [digikey.ch](https://www.digikey.ch)
- **Mouser** — Similar to Digi-Key; good for instruments, connectors, and RF parts. Ships DHL to CH. [mouser.ch](https://www.mouser.ch)
- **Radio / SDR**: RTL-SDR V4 is available directly from [rtl-sdr.com/store](https://www.rtl-sdr.com/store/) or via Mouser.
- **Verify radio compliance**: All RF equipment used in Switzerland must conform to BAKOM regulations. Receive-only devices are generally fine; transmit-capable hardware requires appropriate amateur or commercial licensing.
- **Customs tip**: Orders from outside Switzerland above CHF 62 may be subject to VAT. Digi-Key and Mouser handle EU VAT automatically; check import duties for non-EU shipments.

---

## Contributing

PRs are welcome if the addition:

1. Is **defensive, educational, or general-purpose** — not primarily an offensive or covert-access tool.
2. Includes a clear, practical **description** of the legitimate use case.
3. Links to the **official project or documentation** for software tools.
4. For hardware, links to a reputable retailer (Digitec/Galaxus, Digi-Key, Mouser, or manufacturer) — **not** offensive-security specialty shops.
5. Does **not** duplicate an existing entry without good reason.

Please open an issue first if you're unsure whether an item fits the scope.

---

*Maintained by the community. Use responsibly and lawfully.*