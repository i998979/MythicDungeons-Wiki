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
  # How long will the room invitation expire, in seconds
  InviteExpiration: 60
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
    # **Unimplemented** Hook for FabledParties, party list will be retrieved when creating room if enabled
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
    # Hook for ProSkillAPIParties, party list will be retrieved when creating room if enabled
    ProSkillAPIParties:
      Enabled: false
    # Hook for Talismans, Talismans items can be used if enabled
    Talismans:
      Enabled: false
```
{% endcode %}
