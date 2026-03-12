# Mod List — Meyercraft

## Required

| Mod | Purpose | Link |
|-----|---------|------|
| Fabric Loader | Mod loader (install via installer) | https://fabricmc.net/use/installer/ |
| Fabric API | Core library for Fabric mods | https://modrinth.com/mod/fabric-api |
| Identity | Kill mobs → become them with abilities | https://modrinth.com/mod/identity |
| Fabric Language Kotlin | Dependency for Identity | https://modrinth.com/mod/fabric-language-kotlin |

## Recommended (Performance + QoL)

| Mod | Purpose | Link |
|-----|---------|------|
| Sodium | Massively improves FPS | https://modrinth.com/mod/sodium |
| Lithium | Server/singleplayer tick performance | https://modrinth.com/mod/lithium |
| Mod Menu | Browse and configure mods in-game | https://modrinth.com/mod/modmenu |

## How the Identity Mod Works

1. Find a mob in the world
2. Kill it
3. Press the **Identity key** (default: `~` tilde) to open the identity menu
4. Select the mob you killed — you transform into it
5. You gain that mob's abilities:
   - **Creeper** — charge and explode (you survive)
   - **Bat / Parrot / Bee** — fly
   - **Blaze** — fire immunity + shoot fireballs
   - **Enderman** — teleport
   - **Dolphin** — fast swimming
   - **Wither** — flight + withering touch
   - ...and many more

## Install Steps (PC)

1. **Buy/install Minecraft Java Edition** from minecraft.net (or the launcher)
2. **Run the Fabric Installer** — download from https://fabricmc.net/use/installer/
   - Select the latest Minecraft version
   - Click "Install"
   - This creates a "fabric-loader" profile in your Minecraft launcher
3. **Open your mods folder:**
   - Windows: `%appdata%\.minecraft\mods\`
   - Mac: `~/Library/Application Support/minecraft/mods/`
   - Create the `mods` folder if it doesn't exist
4. **Download and drop in** the JARs from the Required table above (match your MC version)
5. **Launch Minecraft** using the "fabric-loader" profile
6. Go kill some mobs and hit `~` to transform!
