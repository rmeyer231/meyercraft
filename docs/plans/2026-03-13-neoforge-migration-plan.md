# Meyercraft NeoForge Migration — Implementation Plan

> **For Claude:** This is a Prism Launcher setup guide, not a code project. Follow steps sequentially. Verify each step before moving to the next.

**Goal:** Create a new NeoForge 1.21.1 Prism Launcher instance with creature mods (dinosaurs, dragons, sharks, bosses) and the Identity Fix morph system.

**Architecture:** New Prism Launcher instance with NeoForge loader, ~10 NeoForge-native mods, no compatibility layers needed.

**Tech Stack:** Minecraft 1.21.1, NeoForge, Prism Launcher 10.0.5

---

### Task 1: Create NeoForge Instance in Prism Launcher

**Step 1: Create instance**
1. Open Prism Launcher
2. Click **"Add Instance"**
3. Name it: `Meyercraft NeoForge`
4. Select Minecraft version: **1.21.1**
5. Under Mod Loader, select **NeoForge** → pick the latest NeoForge version for 1.21.1
6. Click **OK**

**Step 2: Configure RAM**
1. Right-click `Meyercraft NeoForge` → **Edit** → **Settings** → **Java**
2. Check the memory override box
3. Set **Minimum memory**: `512 MB`
4. Set **Maximum memory**: `6144 MB`
5. Click **Close**

**Step 3: Configure window**
1. In Edit → **Settings** → **Window**
2. Check **"Start maximized"** (prevents the invisible window issue on dual-GPU laptops)

**Step 4: Verify — Launch the bare instance**
1. Double-click to launch
2. Confirm you see the Minecraft main menu (with NeoForge branding)
3. Close the game

---

### Task 2: Install Core Dependencies

All mods are installed via Prism's built-in mod downloader (searches Modrinth + CurseForge).

**Step 1: Open mod manager**
1. Right-click `Meyercraft NeoForge` → **Edit** → **Mods**
2. Click **"Download Mods"**

**Step 2: Install GeckoLib**
- Search: `GeckoLib`
- Select the one by **Gecko** (should show NeoForge 1.21.1 compatible)
- Click Install
- Target version: **4.8.4** or latest for 1.21.1

**Step 3: Install Architectury API**
- Search: `Architectury API`
- Install the NeoForge 1.21.1 version

**Step 4: Install Gabou's Libs**
- Search: `Gabou's Libs` or `gaboulibs`
- Install the NeoForge 1.21.1 version

**Step 5: Verify — Check mods tab**
- You should see 3 mods listed: GeckoLib, Architectury API, Gabou's Libs
- All should show green checkmarks

---

### Task 3: Install Identity Fix (Morph Mod)

**Step 1: Install Identity Fix**
- In Download Mods, search: `Identity Fix`
- Look for the one by **Gabou** (not the original Draylar Identity)
- Install the NeoForge 1.21.1 version (v2.9.4 or later)

**Step 2: Verify — Launch and test**
1. Launch the instance
2. Create a new Creative world (with cheats enabled)
3. Spawn a cow (`/summon minecraft:cow`)
4. Kill it
5. Press **`~`** (tilde) to open the Identity menu
6. Select the cow — you should transform into it
7. If this works, the morph system is good!
8. Close the game

---

### Task 4: Install Creature Mods — Dinosaurs (Priority 1)

**Step 1: Install Jurassic Revived**
- In Download Mods, search: `Jurassic Revived`
- Install for NeoForge 1.21.1 (v0.102.0 or latest)

**Step 2: Verify — Launch and test**
1. Launch the instance
2. Open the same Creative world (or new one)
3. Look for dinosaurs spawning naturally, OR try summoning one
4. Check the mod's entity list — try `/summon` with tab completion to find dino entity names
5. Kill a dinosaur
6. Press `~` — the dinosaur should appear in the Identity menu
7. Transform into it!

**Note:** Jurassic Revived is early development. Some dinos may be missing textures or have buggy AI. This is normal for v0.102.

---

### Task 5: Install Creature Mods — Dragons (Priority 2)

**Step 1: Install IceAndFire Community Edition**
- In Download Mods, search: `Ice and Fire` or `IceAndFire CE`
- Install the NeoForge 1.21.1 version (2.0-beta.11 or latest)
- **Important:** If Prism shows a dependency prompt, accept all dependencies

**Step 2: Verify — Launch and test**
1. Launch the instance
2. In Creative, fly around — dragons spawn naturally in the overworld
3. Or summon one: try tab-completing `/summon iceandfire:`
4. Kill a dragon, press `~`, become a dragon!

**Warning:** IceAndFire dragons are VERY powerful. They burn/freeze entire biomes. In survival, approach with caution. In creative, go wild.

---

### Task 6: Install Creature Mods — Boss Mobs & Sharks

**Step 1: Install Mowzie's Mobs**
- Search: `Mowzie's Mobs`
- Install for NeoForge 1.21.1 (v1.8.1 or latest)

**Step 2: Install Ben's Sharks**
- Search: `Ben's Sharks`
- Install for NeoForge 1.21.1 (v1.2.6 or latest)

**Step 3: Verify — Launch and test**
1. Launch the instance
2. All mods should load without errors
3. Test a shark: fly to an ocean biome, look for sharks, or `/summon` one
4. Test Mowzie's: look for Frostmaw in snowy biomes, or `/summon` with tab completion
5. Kill and morph into each!

---

### Task 7: Install Performance Mods

**Step 1: Install Sodium**
- Search: `Sodium`
- Install the **official** NeoForge 1.21.1 build (v0.6.9 or latest)
- This is the same Sodium from your Fabric setup — it now supports NeoForge natively

**Step 2: Install FerriteCore**
- Search: `FerriteCore`
- Install for NeoForge 1.21.1

**Step 3: Verify — Launch and check FPS**
1. Launch the instance
2. Press F3 to show debug screen
3. Check FPS — should be solid 60+ with your RTX 4070

---

### Task 8: Final Verification & Cleanup

**Step 1: Full mod list check**
Right-click instance → Edit → Mods. You should see approximately:

| # | Mod | Status |
|---|-----|--------|
| 1 | GeckoLib | green |
| 2 | Architectury API | green |
| 3 | Gabou's Libs | green |
| 4 | Identity Fix (Morph) | green |
| 5 | Jurassic Revived | green |
| 6 | IceAndFire CE | green |
| 7 | Mowzie's Mobs | green |
| 8 | Ben's Sharks | green |
| 9 | Sodium | green |
| 10 | FerriteCore | green |

Plus any auto-installed dependencies.

**Step 2: Create the real world**
1. Launch the instance
2. Create a new Survival world
3. Name it something fun (e.g., "Meyercraft Monster World")
4. Enable cheats (so you can grant identities if needed)
5. Play!

**Step 3: Quick-unlock some epic mobs**
Open chat (`T`) and try:
```
/identity grant @s minecraft:ender_dragon
```
For modded mobs, tab-complete the mod namespace:
```
/identity grant @s iceandfire:<tab>
/identity grant @s jurassicrevived:<tab>
/identity grant @s mowziesmobs:<tab>
```

---

## Troubleshooting

**Game crashes on launch after adding a mod:**
- Remove the last mod added (Edit → Mods → select → Remove)
- Relaunch to confirm it was that mod
- Check the mod's page for known incompatibilities

**Identity menu doesn't show modded mobs:**
- Kill the mob first (identity unlock requires a kill)
- Check Identity Fix config for any entity blacklists
- Some GeckoLib-animated mobs may not render correctly when morphed but should still be selectable

**Dinosaurs/dragons not spawning:**
- Some mods need specific biomes or dimensions
- Use `/summon` + tab completion to test if entities exist
- Check mod configs in `.minecraft/config/` folder

**Performance issues with many creature mods:**
- Reduce render distance to 8-10 chunks
- In Sodium settings, lower graphics quality
- Entity-heavy mods can strain even an RTX 4070 with lots of mobs spawned
