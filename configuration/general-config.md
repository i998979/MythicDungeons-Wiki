# General Config

## General

General configuration. These options control everyone in every dungeon.

{% code title="config.yml" lineNumbers="true" fullWidth="false" %}
```yaml
MythicDungeons:
  # Config version, DO NOT MODIFY
  Version: 1
  # Language file the plugin uses, should be located inside locale/
  Language: en_US
  # *** NOT IMPLEMENTED *** If Bungee Mode is enabled, the player joins
  BungeeMode:
    Enabled: false
    Type: Ruins
    WaitRoom:
      world: dungeon
      x: 109.5
      y: 5.0
      z: 242.5
      pitch: 180.0
      yaw: 0.0
  # Delay the dungeon configuration and player data loading
  # If you are using World Generator plugin and having this error
  # "java.lang.NullPointerException: Cannot invoke "org.bukkit.World.getName()"
  # because the return value of "org.bukkit.Location.getWorld()" is null"
  # You may try to turn this on
  LoadDelay: false
  # Restore the dungeon to what it used to look like after the challenge is ended
  RestoreTerrains: true
  # Teleport back players into the dungeon when they left the server and join back during dungeon fight
  # If the server has static spawn, it should be enabled
  TeleportBack: true
  # Where to teleport players after they left and join back the server during dungeon fight
  # Only effective when TeleportBack: true
  # Available options:
  # SPAWN: Teleport back to dungeon's spawn
  # CHECKPOINT: Teleport back to last reached checkpoint
  # PREVIOUS: Teleport back to player's logout location
  TeleportTo: SPAWN
  # Cancel death screen when the player dies
  AutoRespawn: true
  # *** NOT IMPLEMENTED *** Show message to remind player the dungeon is about to end, ascending order, in seconds
  PlaytimeRemind: '60 30 15 5'
  # How long will the dungeon start if the room has enough players, only effective when joining through signs or NPCs
  AutoStartTimer:
  # Show message to remind player the dungeon is about to auto-start, ascending order, in seconds
  AutoStartTimeRemind: '60 30 15 5'
  # Use scoreboard for information display
  UseScoreboard: true
  # How long will the room invitation expire, in seconds
  InviteExpiration: 60
  # Use countdown GUI to allow cancelling pre-starting dungeon
  GUICountdown: true
  # Allow breaking blocks in the dungeon, not including specified blocks in a specified location
  BlockBreak: false
  # Allow placing blocks in the dungeon, not including specified blocks in a specified location
  BlockPlace: false
  # Allow interacting blocks in the dungeon, not including specified blocks in a specified location
  BlockInteract: true
  # Block commands when challenging dungeon
  BlockCommands: true
  # Block PvP when challenging dungeon
  BlockPvP: true
  # Hide messages sent by dungeon challengers from all players
  # Hide messages sent by all players except teammates from dungeon challengers
  HideOtherChat: false
  # Debug message level, 0: no info --- 5: most info
  DebugLevel: 0
  # Command whitelist while BlockCommands is enabled
  # All MythicDungeons commands are whitelisted by default
  Whitelist: [ ]
  # Whitelist:
  # - heal
  # - kill
  # Hook into other plugins for additional features, but it is not necessary
  Hooks:
    # Hook for Vault, money price and rewards can be used if enabled
    Vault:
      Enabled: false
    # Hook for EffectLib, checkpoints will have particle effects if enabled
    EffectLib:
      Enabled: false
    # Hook for HolographicDisplays, checkpoints will have customizable holograms if enabled
    HolographicDisplays:
      Enabled: false
    # Hook for CMI, checkpoints will have customizable holograms if enabled
    CMI:
      Enabled: false
    # Hook for DecentHolograms, checkpoints will have customizable holograms if enabled
    DecentHolograms:
      Enabled: false
    # Hook for MMOCore, party list will be retrieved when creating room if enabled
    MMOCore:
      Enabled: false
    # Hook for MMOItems, MMOItems items can be used in price and rewards if enabled
    MMOItems:
      Enabled: false
    # Hook for ItemsAdder, ItemsAdder items can be used in price and rewards if enabled
    ItemsAdder:
      Enabled: false
    # Hook for EcoItems, EcoItems items can be used in price and rewards if enabled
    EcoItems:
      Enabled: false
    # Hook for EcoArmor, EcoArmor items can be used in price and rewards if enabled
    EcoArmor:
      Enabled: false
    # Hook for Talismans, Talismans items can be used in price and rewards if enabled
    Talismans:
      Enabled: false
    # Hook for ProSkillAPIParties, party list will be retrieved when creating room if enabled
    ProSkillAPIParties:
      Enabled: false
    # Hook for Heroes, party list will be retrieved when creating room if enabled
    Heroes:
      Enabled: false
    # Hook for MythicDrops, MythicDrops items can be used in price and rewards if enabled
    MythicDrops:
      Enabled: false
    # Hook for PlaceholderAPI, PlaceholderAPI placeholders can be used in locale and scoreboard if enabled
    PlaceholderAPI:
      Enabled: false
    # Hook for Citizens, NPCs can be used if enabled
    Citizens:
      Enabled: false
```
{% endcode %}
