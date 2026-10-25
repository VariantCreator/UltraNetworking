# Ultra Networking

**Keep pace with your crew.**

Ultra Networking is built for smoother Valheim multiplayer. It balances world updates, prioritizes active players and creatures, and helps reduce the movement overshoot that makes other players appear to jump around.

Run it on a dedicated server, a game client, or both. BepInEx is the only required dependency.

[Download Ultra Networking](https://github.com/VariantCreator/UltraNetworking/releases/latest)

## Features

- **Balanced world updates.** Gives each connection regular turns to receive changes, with limits on sending work per frame.
- **Priority where it matters.** Favors players, ships and creatures while keeping other world updates moving.
- **Adaptive traffic control.** Adjusts world-update traffic to connection conditions and provides configurable Steam send limits.
- **Optional compression.** Compresses useful Steam packets when Ultra Networking is installed at both ends.
- **Controlled movement prediction.** Limits how far remote players are predicted ahead when their updates stall.

## Installation

1. Install BepInEx for Valheim.
2. Install Ultra Networking through a mod manager, or place `UltraNetworking.dll` in `BepInEx/plugins/UltraNetworking/`.
3. Restart the server or game.

Install on both the server and clients for the full feature set. Server-only installations support players without the mod; compression and remote-player prediction limits require client installation.

Remove Network and other overlapping networking mods before using Ultra Networking.

## Configuration

The config file is created automatically on first launch:

`BepInEx/config/VariantMods.UltraNetworking.cfg`

Each setting includes a description and default value. `Lock Configuration` lets the server control settings on clients running Ultra Networking. Changes saved to the server config reload automatically, and local client values return after disconnecting.

## Compatibility

Ultra Networking works on its own with BepInEx. Gameplay mods and other libraries are optional.

If another mod changes the same networking methods, affected features can pause. The log identifies detected conflicts.

Crossplay uses Valheim's existing PlayFab transport and compression. Update scheduling and world selection still apply; Steam-specific controls do not.

World ownership, inventory data and save formats are unchanged.


