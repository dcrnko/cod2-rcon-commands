## Call of Duty 2 RCON Commands 🎮

This document provides a comprehensive list of RCON (Remote Console) commands for Call of Duty 2 server administration. These commands allow you to manage your server, control gameplay, and interact with players directly from the in-game console.

### How to Use RCON Commands:
1.  Connect to your CoD2 server.
2.  Open the in-game console (usually by pressing the `~` or `` ` `` key).
3.  First, log in to RCON: `/rcon login <YOUR_RCON_PASSWORD>` (replace `<YOUR_RCON_PASSWORD>` with your server's RCON password). You'll typically only need to do this once per session.
4.  After logging in, prefix every command with `/rcon` (e.g., `/rcon say "Hello everyone!"`).


---
## ✅ Core RCON Server Commands
| Command                      | Description                          |
| ---------------------------- | ------------------------------------ |
| `status`                     | Shows player info, ping, score, etc. |
| `map_rotate`                 | Rotates to the next map in rotation  |
| `map_restart`                | Restarts the current map             |
| `map <mapname>`              | Loads specific map                   |
| `kick <playername>`          | Kicks a player                       |
| `clientkick <clientnum>`     | Kicks a player by slot number        |
| `banUser <playername>`       | Bans a player                        |
| `tempbanuser <playername>`   | Temporarily bans player              |
| `unban <playername>`         | Unbans a player                      |
| `say <message>`              | Sends a message to all players       |
| `tell <clientnum> <message>` | Sends a private message              |
| `set <var> <value>`          | Sets a config variable               |
| `seta <var> <value>`         | Sets and archives a variable         |
| `toggle <var>`               | Toggles a cvar between its states    |
| `clear`                      | Clears console output                |

## 🧠 Gameplay Configuration
| Command                       | Description                                   |                       |
| ----------------------------- | --------------------------------------------- | --------------------- |
| `g_gametype <type>`           | Set gametype (`dm`, `tdm`, `ctf`, `hq`, etc.) |                       |
| `g_gravity <value>`           | Set gravity (default: 800)                    |                       |
| `g_speed <value>`             | Set player movement speed                     |                       |
| `g_knockback <value>`         | Adjusts bullet impact force                   |                       |
| \`g\_allowvote <0             | 1>\`                                          | Enable/disable voting |
| \`scr\_allow\_sprint <0       | 1>\`                                          | Enable sprinting      |
| `scr_game_spectatetype <0-2>` | Spectator mode                                |                       |
| \`scr\_teambalance <0         | 1>\`                                          | Auto team balance     |
| `scr_friendlyfire <0-3>`      | Friendly fire settings                        |                       |
| \`scr\_forcerespawn <0        | 1>\`                                          | Force respawn         |
| \`scr\_killcam <0             | 1>\`                                          | Enable killcam        |
| \`scr\_drawfriend <0          | 1>\`                                          | Show teammates        |
| `scr_roundlength <min>`       | Round time                                    |                       |
| `scr_timelimit <min>`         | Match time limit                              |                       |
| `scr_scorelimit <points>`     | Score limit                                   |                       |

## ⚙️ Map and Mode Control
| Command               | Description                  |                  |
| --------------------- | ---------------------------- | ---------------- |
| `map mp_carentan`     | Load Carentan map            |                  |
| `map mp_dawnville`    | Load Dawnville map           |                  |
| `map mp_railyard`     | Load Railyard map            |                  |
| `map mp_toujane`      | Load Toujane map             |                  |
| `map mp_matmata`      | Load Matmata map             |                  |
| `map mp_trainstation` | Load Trainstation map        |                  |
| `map mp_brecourt`     | Load Brecourt map            |                  |
| `map mp_harbor`       | Load Harbor map              |                  |
| `g_mapStartTime`      | Time before the match starts |                  |
| \`g\_doWarmup <0      | 1>\`                         | Enable warmup    |
| `g_warmup <seconds>`  | Warmup duration              |                  |
| \`g\_allowvote <0     | 1>\`                         | Allow map voting |

## 👤 Player Management
| Command                 | Description                      |
| ----------------------- | -------------------------------- |
| `banClient <clientnum>` | Ban by slot                      |
| `kick <name>`           | Kick by name                     |
| `clientkick <num>`      | Kick by slot                     |
| `mutePlayer <num>`      | Mute player                      |
| `unmutePlayer <num>`    | Unmute player                    |
| `listplayers`           | List current players             |
| `name <newname>`        | Change your RCON name            |
| `give <weapon>`         | Give weapon                      |
| `god`                   | Enable godmode (requires cheats) |
| `noclip`                | Enable noclip mode               |

## 🔧 Server Variables
| Command                   | Description        |                       |
| ------------------------- | ------------------ | --------------------- |
| `sv_hostname "<name>"`    | Server name        |                       |
| `sv_maxclients <num>`     | Max players        |                       |
| `sv_privateclients <num>` | Reserve slots      |                       |
| `sv_mapRotation`          | Set map rotation   |                       |
| \`sv\_floodProtect <0     | 1>\`               | Flood protection      |
| `sv_maxRate <num>`        | Max data rate      |                       |
| `sv_timeout <seconds>`    | Connection timeout |                       |
| \`sv\_allowDownload <0    | 1>\`               | Allow file downloads  |
| \`sv\_pure <0             | 1>\`               | Force pure clients    |
| \`sv\_cheats <0           | 1>\`               | Enable cheat commands |

## 🛠️ Weapon and Loadout Config
| Command                      | Description |                       |
| ---------------------------- | ----------- | --------------------- |
| \`scr\_allow\_bar <0         | 1>\`        | Enable BAR            |
| \`scr\_allow\_mp44 <0        | 1>\`        | Enable MP44           |
| \`scr\_allow\_shotgun <0     | 1>\`        | Enable Shotgun        |
| \`scr\_allow\_ppsh <0        | 1>\`        | Enable PPSH           |
| \`scr\_allow\_mg42 <0        | 1>\`        | Enable MG42           |
| \`scr\_allow\_panzerfaust <0 | 1>\`        | Enable Panzerfaust    |
| \`scr\_allow\_grenades <0    | 1>\`        | Enable grenades       |
| \`scr\_allow\_smoke <0       | 1>\`        | Enable smoke grenades |
| \`scr\_allow\_bazooka <0     | 1>\`        | Enable bazookas       |

## 📊 Match Control & Scoreboard
| Command                    | Description          |                               |
| -------------------------- | -------------------- | ----------------------------- |
| `scoreboard`               | Show live scoreboard |                               |
| `pause`                    | Pause game           |                               |
| `unpause`                  | Unpause game         |                               |
| `resetMatch`               | Reset match score    |                               |
| \`g\_compassShowEnemies <0 | 1>\`                 | Show enemies on radar         |
| \`g\_teamautojoin <0       | 1>\`                 | Auto-assign teams             |
| \`g\_redCrosshairs <0      | 1>\`                 | Show red aim cross on enemies |

## 🔎 Debugging and Logs
| Command                | Description         |                         |
| ---------------------- | ------------------- | ----------------------- |
| \`logfile <0           | 1>\`                | Enable log file         |
| `g_log <filename>`     | Set log file name   |                         |
| \`g\_logSync <0        | 1>\`                | Sync log file writing   |
| \`developer <0         | 1>\`                | Enable developer mode   |
| \`developer\_script <0 | 1>\`                | Enable script debugging |
| `dumpuser <clientnum>` | Dump user data      |                         |
| `record <name>`        | Record a demo       |                         |
| `stoprecord`           | Stop demo recording |                         |

## 🎮 Fun / Custom / Cheats (for testing)
| Command               | Description                   |                     |
| --------------------- | ----------------------------- | ------------------- |
| `give all`            | Give all weapons              |                     |
| \`cg\_thirdPerson <0  | 1>\`                          | Third-person camera |
| `timescale <value>`   | Game speed (1.0 = normal)     |                     |
| `cg_fov <value>`      | Field of view                 |                     |
| `notarget`            | Enemies ignore you (SP)       |                     |
| `ufo`                 | Spectator-style free movement |                     |
| `toggle r_fullscreen` | Toggle fullscreen             |                     |
| `vid_restart`         | Restart video settings        |                     |

## 🗺️ Maps List (for map command)
| Map Code          | Map Name     |
| ----------------- | ------------ |
| `mp_carentan`     | Carentan     |
| `mp_dawnville`    | Dawnville    |
| `mp_brecourt`     | Brecourt     |
| `mp_harbor`       | Harbor       |
| `mp_matmata`      | Matmata      |
| `mp_railyard`     | Railyard     |
| `mp_toujane`      | Toujane      |
| `mp_trainstation` | Trainstation |
| `mp_decoy`        | Decoy        |
| `mp_leningrad`    | Leningrad    |

## 📌 Tips
Always set the rcon password before issuing commands:
rcon password mysecurepassword

You can bind keys for common commands:
bind F3 "rcon say Hello, players!"
