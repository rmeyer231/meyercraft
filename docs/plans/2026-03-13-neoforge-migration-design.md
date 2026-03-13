# Meyercraft NeoForge Migration Design

**Date:** 2026-03-13
**Goal:** Migrate from Fabric to NeoForge 1.21.1 to unlock giant creature mods (dinosaurs, dragons, kaiju) while keeping the Identity morph system.

## Decision

Switch from Fabric to NeoForge 1.21.1 in a new Prism Launcher instance. The existing Fabric instance stays as a fallback.

Key discovery: **Identity Fix (Morph)** has native NeoForge support, eliminating the need for Sinytra Connector.

## Priorities

1. Dinosaurs (T-Rex, Velociraptor, etc.)
2. Giant Dragons (fire/ice, mythical creatures)
3. Godzilla/Kaiju (unavailable for 1.21.1 — substituted with epic boss mobs)

## Mod List

### Core Dependencies

| Mod | Version | Purpose |
|-----|---------|---------|
| NeoForge Loader | 1.21.1 | Mod loader |
| GeckoLib | 4.8.4 | Animation library for creature mods |
| Architectury API | latest 1.21.1 | Cross-loader library (Identity Fix dep) |
| Gabou's Libs | latest 1.21.1 | Identity Fix dependency |

### The Morph Mod

| Mod | Version | Purpose |
|-----|---------|---------|
| Identity Fix (Morph) | 2.9.4+ | Kill mobs, become them, gain abilities |

### Creature Mods (Priority Order)

| Mod | Version | What It Adds |
|-----|---------|-------------|
| Jurassic Revived | 0.102.0 | 40+ dinosaurs: T-Rex, Velociraptor, Triceratops, Pteranodon |
| IceAndFire CE | 2.0-beta.11 | Fire/Ice Dragons, Hippogryphs, Gorgons, Sirens, Death Worms, Trolls |
| Mowzie's Mobs | 1.8.1 | Naga, Frostmaw, Barako — epic giant boss creatures |
| Ben's Sharks | 1.2.6 | 26 shark species including Megalodon, Great White |

### Performance

| Mod | Version | Purpose |
|-----|---------|---------|
| Sodium | 0.6.9 (official NeoForge) | FPS boost |
| FerriteCore | 7.1.2 | Memory usage reduction |

## Not Available for 1.21.1

- **Kaiju Calamity** (Godzilla) — Forge 1.20.1 only
- **Thalassophobia** (leviathans) — Forge 1.20.1 only
- **Hybrid Aquatic** — Fabric only (could use Connector but adds complexity)

## Architecture

- New Prism Launcher instance: "Meyercraft NeoForge"
- NeoForge 1.21.1 loader
- ~10 mods total
- Existing Fabric "Meyercraft" instance preserved as fallback
- No Sinytra Connector needed

## Risks

- Jurassic Revived is early development (v0.102.0) — expect some bugs
- IceAndFire CE is beta — don't upgrade mid-save without backup
- Ben's Sharks NeoForge port has some broken effects
- Identity Fix may not animate all GeckoLib creatures perfectly when morphed

## RAM Allocation

- Keep at 6144 MB (6 GB) — same as current Fabric instance
- More creature mods = more entities = more RAM needed
