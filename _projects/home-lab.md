---
title: Home Lab
description: "A refurbished old PC turned NAS, now running TrueNAS with ZFS, Immich for photos and Tailscale for remote access."
period: "2025 – Present"
sort_date: 2025-01-01 # TODO: set the real start month if you want finer ordering
ongoing: true
category: Other
featured: true
tags: [TrueNAS, ZFS, Immich, Tailscale]
---

## How it started

The homelab started life as a SUPER OLD PC that I refurbished into a NAS by installing TrueNAS on it. The catch: it only had 2GB of RAM... RAMageddon fr. The plan back then was to add more RAM, set up Pi-hole on a Raspberry Pi I borrowed from a friend, and install Jellyfin for media hosting once the RAM situation was sorted.

<!-- TODO: how that turned out — did the RAM upgrade, Pi-hole and Jellyfin happen? -->

These days it runs TrueNAS with ZFS, Immich and Tailscale. Here's the [current setup](#current-setup).

## Current setup

- **TrueNAS** with **ZFS** for storage
- **Immich** for self-hosted photo backup
- **Tailscale** so I can reach it from anywhere without opening ports

<!-- TODO: hardware specs, pool layout (mirror? RAIDZ?), and anything you learnt setting it up. -->
