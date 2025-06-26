# 🎯 Item Multiplier - PEAK Game Mod

**Boost your loot in PEAK! Configurable item spawn multiplier with focus on luggages.**

## 🔥 Features

- **📦 2x Default Multiplier** - Balanced boost for Luggage loot
- **⚙️ Fully Configurable** - Set any multiplier (2x, 5x, 10x, 100x!)
- **🎯 Selective Spawners** - Enable/disable different spawner types
- **🌐 Multiplayer Compatible** - Works in co-op (host needs mod)

## 📊 Default Configuration

```ini
[General]
ItemMultiplier = 2          # 2x items by default

[Spawner Types]
EnableLuggage = true        # ✅ Chests give 2x loot
EnableRespawnChest = false  # ❌ RespawnChests normal
EnableBerryBush = false     # ❌ Berry bushes normal
EnableBerryVine = false     # ❌ Berry vines normal
EnableGroundSpawner = false # ❌ Ground spawners normal
```

## 🚀 Installation

### Manual
1. Install [BepInEx 5.4.21](https://github.com/BepInEx/BepInEx/releases)
2. Download `ItemMultiplierMod.dll`
3. Place in `BepInEx/plugins/` folder
4. Launch game

## ⚙️ Configuration

Edit `BepInEx/config/com.peak.itemmultiplier.cfg`:

### Multiplier Settings
- `ItemMultiplier = 2.0` → 2x items (default)
- `ItemMultiplier = 5.0` → 5x items
- `ItemMultiplier = 10.0` → 10x items

### Spawner Types
- `EnableLuggage = true` → Luggage affected
- `EnableBerryBush = true` → Berry bushes affected
- `EnableGroundSpawner = true` → Ground items affected

### 🌐 Multiplayer
- **Host has mod:** Everyone benefits
- **Client has mod:** No effect (host needs it)

## ⚠️ Important Notes

### Performance
- High multipliers (10x+) may cause lag
- Many items = more physics calculations

### Balance
- Default 2x is balanced for normal gameplay
- Higher multipliers change game difficulty
- Coordinate with friends in multiplayer

### Compatibility
- **Requires:** BepInEx 5.4.21+
- **Compatible:** Most other PEAK mods
- **Multiplayer:** Host must have mod installed

## 🐛 Troubleshooting

### Mod Not Working
1. Check BepInEx installation
2. Verify `ItemMultiplierMod.dll` in plugins folder
3. Check console for errors
4. Write me - discord:icetypes -

### No Extra Items
1. Ensure `EnableLuggage = true`
2. Check multiplier value > 1.0
3. Host needs mod in multiplayer

### Performance Issues
1. Lower multiplier value
2. Disable optional spawner types
3. Check system specs

## 📄 License

This mod is released under MIT License. Feel free to modify and redistribute.

---

**Enjoy your boosted loot in PEAK! 🎉**