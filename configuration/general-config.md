# General Config

## General

General configuration. These options control everyone in every dungeon.

{% code title="config.yml" lineNumbers="true" fullWidth="false" %}
```yaml
MythicDungeons:
  # Config version, DO NOT MODIFY
  Version: 2
  # Language file the plugin uses, should be located inside locale/
  Language: en_US
  # Save scoreboard created by other plugin and revert after dungeon scoreboard is removed
  SaveExternalScoreboard: false
  # Hide scoreboard numbers on right side, only effective on 1.20.3+
  HideScoreboardNumber: false
  # How long will the room invitation expire (in seconds)
  InviteExpiration: 60
  # How long will the room disband/members be removed if the owner/member has been disconnected (in seconds)
  DisconnectRemoval: 60
  # Default input method if string input is required, available options are SIGN, ANVIL, CHAT
  DefaultInputMethod: SIGN
  # Debug message level, 0: no info --- 5: most info
  DebugLevel: 0
  # Hook into other plugins for additional features, but it is not necessary
  Hooks:
    # Hook for CMI, holograms will be shown above objectives if enabled
    CMI:
      Enabled: false
    # Hook for DecentHolograms, holograms will be shown above objectives if enabled
    DecentHolograms:
      Enabled: false
    # Hook for EcoArmor, EcoArmor items can be used if enabled
    EcoArmor:
      Enabled: false
    # Hook for EcoItems, EcoItems items can be used if enabled
    EcoItems:
      Enabled: false
    # Hook for FabledParties, party list will be retrieved when creating room if enabled
    FabledParties:
      Enabled: false
    # Hook for Heroes, party list will be retrieved when creating room if enabled
    Heroes:
      Enabled: false
    # Hook for HolographicDisplays, holograms will be shown above objectives if enabled
    HolographicDisplays:
      Enabled: false
    # Hook for ItemsAdder, ItemsAdder items can be used if enabled
    ItemsAdder:
      Enabled: false
    # Hook for MMOCore, party list will be retrieved when creating room if enabled
    MMOCore:
      Enabled: false
    # Hook for MMOItems, MMOItems items can be used if enabled
    MMOItems:
      Enabled: false
    # Hook for MythicDrops, MythicDrops items can be used if enabled
    MythicDrops:
      Enabled: false
    # Hook for Parties, party list will be retrieved when creating room if enabled
    Parties:
      Enabled: false
    # Hook for Talismans, Talismans items can be used if enabled
    Talismans:
      Enabled: false
```
{% endcode %}
