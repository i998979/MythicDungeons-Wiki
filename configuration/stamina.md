---
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Stamina

Stamina acts like another type of currency, but it will recover over time.

Different Dungeon Group can have different stamina configurations. If Dungeon Group is charging stamina, but no corresponding stamina definition was found, the `default` branch will be used.

It can have different configurations depending on the permissions the player has, the first branch with matching permissions will be selected. If no matching permission was found, the `default` branch will be used and the `default` stamina will be deducted.

Keep only the default branch and adjust values if global stamina is used.

{% code title="stamina.yml" %}
```yaml
Stamina:
  # Stamina definitions for specific dungeon groups
  Ruins:
    # Permission-based stamina configuration. If no permission matches, fallback to 'default'
    '0':
      # Permission required
      Permission: 'MythicDungeons.VIP'
      # Maximum stamina points a player can have
      Limit: 200
      # Duration of one recovery cycle (in seconds)
      Time: 1
      # Stamina points recovered per cycle
      Recover: 1
      # Whether stamina continues recovering if the player is offline
      RecoverIfOffline: true
    # Fallback branch for players without permissions
    default:
      Limit: 100
      Time: 1
      Recover: 1
      RecoverIfOffline: true
  RuinsSimplified:
    '0':
      Permission: 'MythicDungeons.VIP'
      Limit: 200
      Time: 60
      Recover: 50
      RecoverIfOffline: true
    default:
      Limit: 100
      Time: 60
      Recover: 10
      RecoverIfOffline: true
  # Default configuration for any dungeon group not defined
  default:
    default:
      Limit: 0
      Time: 1
      Recover: 0
      RecoverIfOffline: true

```
{% endcode %}
