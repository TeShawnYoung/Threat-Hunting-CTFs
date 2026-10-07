# Threat Hunting CTFs

## Project Overview

This repository showcases **capture-the-flag (CTF) style threat hunting challenges** completed across various platforms and ranges, focused on hands-on detection, log analysis, and adversary technique identification in a scored, objective-driven format.

Unlike open-ended lab scenarios, each entry here is built around a specific set of challenge objectives ("flags") to be captured — testing the ability to quickly pull signal from logs and telemetry under a defined set of questions rather than a freeform investigation.

Each write-up includes the platform/range used, tools leveraged, the flags captured, the queries or techniques used to solve them, and key takeaways from the challenge.

---

## Core Threat Hunting CTF Challenges

### 1. 🚩 Threat Hunt CTF Report: Password Spray to Lateral Movement (NPT-WS01) <a href="https://github.com/TeShawnYoung/Threat-Hunt-CTF-Report-Password-Spray-to-Lateral-Movement-NPT-WS01-/blob/main/README.md"><img src="https://img.shields.io/badge/--555555?style=flat&logo=github&logoColor=white" height="20"/></a>

**Focus:** Investigating overnight login prompts on a Finance workstation, which turned out to be a Remote Desktop password spray followed by implant execution, persistence and movement toward a second host.

**Platforms and Languages Leveraged:**

* Windows Server 2022 Virtual Machines (Microsoft Azure)
* EDR Platform: Microsoft Defender for Endpoint
* Kusto Query Language (KQL)

**Key Capabilities:**

* Logon event analysis to identify the compromised account and the attacker's source IP
* Process tree analysis to confirm remote WMI execution of the implant
* Network and file event analysis to find the C2 domain and the dropped implant's hash
* Persistence hunting across Run keys, scheduled tasks, services and local accounts
* Cross-host scoping with alert evidence, and a NIST 800-61 containment plan

**Resources:**

* 📄 [Threat Hunt CTF Report](https://github.com/TeShawnYoung/Threat-Hunt-CTF-Report-Password-Spray-to-Lateral-Movement-NPT-WS01-/blob/main/README.md)
* 🔎 [KQL Queries & Steps Taken](https://github.com/TeShawnYoung/Threat-Hunt-CTF-Report-Password-Spray-to-Lateral-Movement-NPT-WS01-/blob/main/README.md#steps-taken)
* 🗓️ [Event Timeline](https://github.com/TeShawnYoung/Threat-Hunt-CTF-Report-Password-Spray-to-Lateral-Movement-NPT-WS01-/blob/main/README.md#event-timeline)
* 🎯 [MITRE ATT&CK Mapping](https://github.com/TeShawnYoung/Threat-Hunt-CTF-Report-Password-Spray-to-Lateral-Movement-NPT-WS01-/blob/main/README.md#mitre-attck-ttp-alignment)
* 🛠️ [Response Taken](https://github.com/TeShawnYoung/Threat-Hunt-CTF-Report-Password-Spray-to-Lateral-Movement-NPT-WS01-/blob/main/README.md#response-taken)

<!--
Template for the next entry. Duplicate this block for each new challenge.

### #. 🚩 [Report title]

**Focus:** One sentence on what the challenge scenario covers.

**Platforms and Languages Leveraged:**

* [e.g. Microsoft Defender for Endpoint, Splunk, KQL]

**Key Capabilities:**

* [Up to five short lines on the analysis done]

**Resources:**

* 📄 [Threat Hunt CTF Report](link)
* 🔎 [KQL Queries & Steps Taken](link#steps-taken)
* 🗓️ [Event Timeline](link#event-timeline)
* 🎯 [MITRE ATT&CK Mapping](link#mitre-attck-ttp-alignment)
* 🛠️ [Response Taken](link#response-taken)
-->

---

## Technical Architecture & Workflow

1. **Challenge Intake**
   Review the scenario briefing and defined flags/objectives for the CTF room or range.

2. **Data Review**
   Work through the provided logs, packet captures, memory images, or telemetry relevant to the platform.

3. **Flag Discovery**
   Apply targeted queries and analysis techniques to answer each flag's specific question.

4. **Technique Mapping**
   Where applicable, map discovered activity to MITRE ATT&CK tactics and techniques.

5. **Write-up**
   Document tools used, queries run, flags captured, and lessons learned for future reference.

---

## Skills Demonstrated

* **Threat Hunting:** Objective-driven log and telemetry analysis under time/scoring constraints
* **Log Analysis:** Working across varied log sources and SIEM/EDR platforms
* **Query Development:** Building targeted queries to answer specific investigative questions
* **MITRE ATT&CK Mapping:** Aligning observed activity to known adversary tactics and techniques
* **Tool Proficiency:** Hands-on use of common blue team tooling across multiple ranges and platforms
* **Technical Writing:** Communicating findings and methodology in a clear, repeatable format
