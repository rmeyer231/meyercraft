# Troubleshooting

## Game Crashes on Launch

**Most common cause:** Mod version mismatch. Every mod must match your Minecraft version exactly.
- Minecraft 1.21.4 needs mods built for 1.21.4, not 1.21.1
- Prism Launcher filters this automatically when you search for mods — manual downloads don't

**Check the crash log:**
- Windows: `%appdata%\.minecraft\crash-reports\`
- Or in Prism: right-click instance → **View Logs**
- Search the log for `Caused by:` — that's usually the broken mod
- Remove that mod and relaunch

## Out of Memory / Laggy

Modded Minecraft needs more RAM than vanilla.

**In Prism Launcher:**
1. Right-click instance → **Edit** → **Settings** → **Java**
2. Set **Maximum memory allocation** to `4096 MB` (4 GB)
3. If you have 16+ GB of system RAM, go to `6144 MB` (6 GB)

**Don't allocate too much** — giving it 8+ GB actually makes it slower (garbage collector thrashing). 4-6 GB is the sweet spot for a moderate mod list.

## Mod Conflicts

If the game crashes after adding a new mod:
1. Remove the last mod you added
2. Relaunch — if it works, that mod conflicts with something
3. Check the mod's page on Modrinth for known incompatibilities

## Identity Mod Not Working

- **Can't open the menu:** Default key is `~` (tilde). Check Options → Controls → search "identity"
- **Killed a mob but can't transform:** Some mobs require config changes. Check `.minecraft/config/identity/`
- **Abilities not working:** Some abilities need you to press a secondary key (like crouch + ability key). Check the mod's wiki on Modrinth

## World Corruption

Modded worlds can occasionally corrupt, especially if the game crashes mid-save. **Always keep backups** — see the backup guide below.

## Java Version Issues

Minecraft 1.20.5+ requires **Java 21**. Prism Launcher bundles the right Java version automatically. If using the vanilla launcher, you may need to install Java 21 manually from https://adoptium.net.
