# Peak Lobby Fix

A BepInEx mod for PEAK that fixes Steam lobby join timing issues.

## Problem

When joining PEAK through Steam lobby links (`steam://joinlobby`):
- The game immediately tries to join the lobby
- But Photon networking isn't connected yet
- Results in "Photon Room not found" error and infinite loops

## Solution

This mod:
- Intercepts Steam lobby join attempts
- Waits for Photon to fully connect
- Automatically joins the lobby once ready
- Includes timeout protection (10 seconds)

## Installation

### Manual Installation
1. Make sure BepInEx is installed
2. Download the latest release
3. Extract to `BepInEx/plugins/` folder
4. Launch PEAK

## Features

- ✅ Fixes Steam lobby join timing issues
- ✅ Waits for Photon connection before joining
- ✅ Timeout protection (prevents infinite waiting)
- ✅ Detailed logging for troubleshooting
- ✅ Automatic retry system
- ✅ Compatible with other PEAK mods

## How It Works

1. **Detection**: Monitors Steam lobby join requests
2. **Validation**: Checks if Photon is connected and authenticated
3. **Delay**: If not ready, delays the join attempt
4. **Execution**: Automatically joins when Photon is ready
5. **Cleanup**: Resets state after successful join

## Technical Details

The mod uses Harmony patches to intercept:
- `SteamLobbyHandler.TryJoinLobby()` - Direct lobby join attempts
- `SteamLobbyHandler.OnLobbyJoinRequested()` - Steam callback joins
- `NetworkConnector.OnConnectedToMaster()` - Connection status tracking

## Troubleshooting

### Mod not working
- Ensure BepInEx is properly installed
- Check `BepInEx/LogOutput.log` for errors
- Verify mod is in `BepInEx/plugins/` folder

### Still can't join lobbies
- Check Photon connection status in logs
- 10-second timeout may have expired
- Try joining again after game fully loads

- Write me in discord: icetypes

### Compatibility
This mod is compatible with other PEAK mods. It only affects lobby join timing.

## Logs

Look for these messages in BepInEx console:
- `Peak Lobby Fix Mod loaded - Simple approach!`
- `Photon not ready, delaying lobby join for: [ID]`
- `Photon is ready! Processing delayed lobby join...`
- `Successfully initiated delayed lobby join!`

## Configuration

No configuration needed - the mod works automatically.

## Support

If you encounter issues:
1. Check BepInEx logs
2. Report bugs with log files
3. Join the PEAK modding community

## Changelog

### 1.0.0
- Initial release
- Fixed Steam lobby join timing issues
- Added Photon connection waiting
- Implemented timeout protection
