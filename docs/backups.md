# World Backups

Kids pour hours into their worlds. Modded Minecraft is less stable than vanilla. Back up regularly.

## Where Worlds Are Stored

- **Windows:** `%appdata%\.minecraft\saves\`
- **Mac:** `~/Library/Application Support/minecraft/saves/`
- **Prism Launcher:** Each instance has its own saves folder — right-click instance → **Folder** → `saves/`

## Manual Backup

Just copy the world folder somewhere safe. Each world is its own folder inside `saves/`.

```
saves/
  MyWorld/         ← copy this whole folder
    level.dat
    region/
    ...
```

## When to Back Up

- Before adding or removing mods
- Before updating Minecraft or Fabric
- After a big build session (if your kid just spent 2 hours building a castle, back it up)
- Weekly at minimum

## Automatic Backups (In-Game)

Install the **FTB Backups** mod — it auto-saves world backups on a timer:

| Mod | Link |
|-----|------|
| FTB Backups | https://modrinth.com/mod/ftb-backups |

Configure it in `.minecraft/config/` to set backup frequency and how many to keep.

## If a World Gets Corrupted

1. Close Minecraft completely
2. Go to `saves/` and rename the corrupted world folder (e.g., `MyWorld` → `MyWorld_broken`)
3. Copy your most recent backup into `saves/`
4. Relaunch — the backup should load

If you don't have a backup, try the **NBT Explorer** tool to repair `level.dat`: https://github.com/jaquadro/NBTExplorer
