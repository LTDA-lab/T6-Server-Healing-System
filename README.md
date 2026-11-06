# T6 MP – Advanced Healing System

**Custom GSC Script for Call of Duty: Black Ops II – Plutonium Multiplayer**

A custom server-side healing system designed for T6 Multiplayer dedicated servers. Introduces manual health regeneration, temporary weapon restrictions, consecutive healing detection, cooldown management, and dynamic HUD notifications.

## Features

- **Manual Healing:** Players can manually restore health by holding the `[F]` key.
- **Progressive Health Regeneration:** Restores 15 HP every 0.05 seconds until maximum health is reached.
- **Healing Animation:** Temporarily disables weapons and player interactions during the healing process.
- **Minimum Healing Duration:** Enforces a minimum healing duration of 1 second, even if the player releases the key earlier.
- **Consecutive Healing Detection:** Tracks consecutive healing attempts within a 3-second interval.
- **Healing Cooldown:** Activates a 5-second cooldown after two consecutive healing uses.
- **Dynamic HUD Notifications:** Displays contextual messages for healing availability, damage alerts, and cooldown status.
- **Damage Detection:** Automatically displays a healing prompt when the player receives damage.
- **Automatic State Reset:** Resets healing variables and restores weapon functionality upon respawn.
- **Per-Player System:** Each player has independent healing states, cooldowns, and monitoring threads.

## Configuration

The following parameters can be adjusted directly in the `monitor_heal()` function:

| Parameter | Default | Description |
|---|---:|---|
| `heal_rate` | 15 | Health restored per tick |
| `max_consecutive_uses` | 2 | Consecutive healing uses before cooldown |
| `max_interval_ms` | 3000 | Maximum interval between healing attempts |
| `cooldown_time` | 5 | Cooldown duration in seconds |
| `min_anim_time` | 1.0 | Minimum healing duration in seconds |

## Healing Mechanics

1. The player takes damage and receives a HUD notification.
2. The player holds `[F]` to initiate healing.
3. Weapons and default interactions are temporarily disabled.
4. Health is progressively restored until maximum health is reached.
5. Weapons and interactions are re-enabled.
6. After two consecutive healing uses within 3 seconds, a 5-second cooldown is activated.

## Compatibility

- **Game:** Call of Duty: Black Ops II
- **Mode:** Multiplayer (T6)
- **Platform:** Plutonium
- **Script Language:** GSC
- **Execution:** Server-Side

## License

Free to use and modify. Credit to the original author is appreciated.

---

**Custom gameplay modification for Plutonium T6 Multiplayer dedicated servers.**
