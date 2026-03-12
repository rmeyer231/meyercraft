# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Meyercraft** is a custom Minecraft Java Edition modded setup for Randy and his son. The primary goal is a modded experience where the player can transform into any mob with full abilities (fly as a bat, explode as a creeper, swim as a guardian, etc.).

## Target Platform

- **Edition:** Minecraft Java Edition (latest stable)
- **Mod Loader:** Fabric
- **Play Style:** Single-player or LAN on Randy's PC
- **Primary Mod:** Identity mod (Draylar) — kill mobs to unlock their forms and abilities

## Directory Structure

- `mods/` — Fabric mod JARs to install into `.minecraft/mods/`
- `config/` — Mod configuration files
- `resourcepacks/` — Custom resource packs (if any)
- `server/` — Server files (if LAN/dedicated server is set up)
- `docs/` — Install guides and notes

## Key Commands

These will be relevant once the server component is set up:

```bash
# Start a local Fabric server (from server/ directory)
java -Xmx4G -Xms2G -jar fabric-server-launch.jar nogui

# Download mods via packwiz (if adopted)
packwiz refresh
```

## Mod Stack

See `docs/mod-list.md` for the full mod list with versions and download links.

Core mods:
- **Fabric API** — required library for all Fabric mods
- **Identity** — transform into any mob you kill, gain their abilities
- **Fabric Language Kotlin** — dependency for some mods

Quality-of-life mods (optional):
- **Sodium** — performance boost
- **Lithium** — server-side performance
- **Mod Menu** — in-game mod configuration UI
