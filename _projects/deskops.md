---
title: DeskOps
description: "A hands-on OT security training platform built to give students their first touch-point with industrial control system security."
period: "2025 – Present"
sort_date: 2025-09-01
ongoing: true
category: OT Security
featured: true
tags: [OT/ICS, Purdue Model, IEC 62443, MITRE ATT&CK for ICS, OPNsense]
---

## Why

DeskOps is the biggest project I've taken on so far. It started when I wanted to learn OT security and found there wasn't much hands-on learning I could do on my own. Most of it is theory, and the hands-on options are geared towards working professionals. Compared to IT security, there's a much bigger accessibility gap for students.

So I formed a team of five, and we've been building an OT security training platform that gives students a first touch-point into OT security.

<!-- TODO: a sentence or two on who DeskOps is for and what a student walks away with. -->

## Architecture

The lab is laid out along the Purdue Model, so students can see where each device sits and how traffic is meant to flow between levels.

<!-- TODO: list which Purdue levels are built out and what lives at each (e.g. Level 0–1 PLCs, Level 2 HMI, Level 3 historian…). -->

- **OPNsense at the IT/OT boundary** — the firewall between the enterprise and control networks.
- **Open vSwitch VLANs** — segment the network inside the lab.

<figure>
  <img src="{{ '/assets/img/deskops-architecture.webp' | relative_url }}" width="1789" height="2000" loading="lazy" alt="DeskOps architecture mapped to the Purdue Model. Level 4–5 (Enterprise/IT): a Kali Linux attacker acting as a compromised IT host. Level 3.5 (IT/OT boundary): a firewall routing between all VLANs. Level 3 (Operations): an Open vSwitch switch carrying VLANs 10, 20 and 30, and a Windows engineering workstation on VLAN 20 with RDP on port 3389. Level 2 (Supervisory): a FUXA HMI on VLAN 10, port 1881. Level 1 (Basic control): an OpenPLC PLC on VLAN 30 speaking Modbus TCP on port 502. Level 0 (Process): simulated field devices, a level sensor and pump, hardwired to the PLC. A dashed line shows a passive mirror from the switch to the Kali host.">
  <figcaption>DeskOps architecture across the Purdue Model levels.</figcaption>
</figure>

## Attack-and-defend scenarios

DeskOps has seven attack-and-defend scenarios. Each attack is mapped to MITRE ATT&CK for ICS, and the defences are built around IEC 62443 zones and conduits.

<!-- TODO: list the seven scenarios, e.g.
| # | Scenario | ATT&CK for ICS technique | Defence |
|---|----------|--------------------------|---------|
| 1 | …        | T0xxx …                  | …       |
-->

## Backing

- **PUB** — validation of the platform. <!-- TODO: one line on what PUB validated. -->
- **Schneider Electric** — sponsored PLCs for the lab.
- **Cyber Security Agency of Singapore (CSA)** — a $7,340 CTDF grant to host a DeskOps workshop in January 2027.

We're also in touch with MSE and PSA. <!-- TODO: still accurate? -->

## What's next

Migrating DeskOps to AWS so students can access the lab straight from their browser.

<!-- TODO: link to a repo, demo or workshop page if you want one here (use `links:` in the front matter). -->
