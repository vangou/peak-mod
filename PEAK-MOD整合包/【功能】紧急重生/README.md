# Revive Hotkey

Revive yourself with the press of a button.

This mod adds a single, lightweight feature to PEAK:
- Press a configurable key (default: `Z`) to revive your character **only when unconscious**.
- A configurable **revive limit** is now supported — default is infinite.

## 🔧 Configuration

After running the game once with this mod installed, a config file will be generated at:

```
BepInEx/config/com.revivehotkey.cfg
```

You can edit this file to change your settings:

```ini
[General]
## Key used to revive yourself when unconscious
ReviveKey = Z

## How many times you can use the revive key (-1 = infinite)
ReviveLimit = -1
```

Set the revive key to any valid `KeyCode` (like `R`, `F`, `Space`, etc.).  
Change `ReviveLimit` to any positive number to enforce a limit.

## 💡 How It Works

- Only functions when your character is **fully unconscious** (not standing, not ragdolled, not dead).
- Blocks usage when **dead**.

## ⚠️ Known Issues

- None currently reported.

## 📦 Installation

1. Download **BepInEx for PEAK** from [Thunderstore](https://thunderstore.io/c/peak/p/BepInEx/BepInExPack_PEAK/)
2. Extract the contents of that `.zip` into your game directory:  
   `C:\Program Files (x86)\Steam\steamapps\common\PEAK`
3. Launch the game once, then close it again — this completes BepInEx’s setup.
4. Navigate to:  
   `...\PEAK\BepInEx\plugins`
5. Copy `ReviveHotkey.dll` from the mod release into that `plugins` folder.
6. Run the game. You’re done!

Enjoy!
