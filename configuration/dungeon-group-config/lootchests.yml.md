# lootchests.yml

```yaml
# Loot chests that players can get items from it
LootChests:
  # ID of the loot chest, must be unique
  '1':
    Name: "&eTreasure Chest"
    # Location of the loot chest
    Location:
      world: dungeon
      x: 125.0
      y: 5.0
      z: 260.0
    # Particle effects of the loot chest, only effects declared in "effects.yml" can be used
    Effects:
      # Appear when the loot chest is not opened
      Idle:
        - vortex 3.0
      # Appear when the loot chest is opened and not renewable
      Opened:
        - vortex 3.0
      # Appear when the loot chest is opened and waiting for renewal
      Renew:
        - vortex 3.0
    Hologram:
      Idle:
        # Vertical offset of the hologram based on the original location
        Offset: 4.0
        Lines:
          - '{material=PLAYER_HEAD;glow=true;damage=0;skullowner=991d961c-b6b4-4d49-88e6-01788cf445dc}'
          - '&fOPEN ME!'
      Opened:
        Offset: 6.0
        Lines:
          - '{material=PLAYER_HEAD;glow=true;damage=0;skullowner=3fb398fb-f50a-42de-998d-692c35048e86}'
          - '&7CLAIMED'
      Renew:
        Offset: 2.0
        Lines:
          - '{material=PLAYER_HEAD;glow=true;damage=0;skullowner=34a35801-3895-4aae-a7e5-fbb52e575e3d}'
          - '&7RENEW IN %time%'
    Potions:
      - SPEED 10 2 true true true
      - JUMP 10 2 true true true
    # Type of the loot chest, check here for available inventory type
    # https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/inventory/InventoryType.html
    Type: CHEST
    # Whether every player in the dungeon has their loot chest inventory, or they share the same one
    PerPlayer: true
    # How long(in ticks) will the loot chest renews
    Renew: 60
    # Title of the loot chest, empty if default title should be used
    Title: ''
    # Size of the loot chest when "Type" is "CHEST"
    Size: 54
    # Contents of the loot chest
    # Use "/mg check" with the items on your hand to retrieve the string
    # Followed by which slot to put
    Items:
      - '{"v":2865,"type":"REDSTONE_BLOCK"} 8'
      - '{"v":2865,"type":"DIAMOND_BLOCK"} 16'
      - '{"v":2865,"type":"EMERALD_BLOCK"} 24'
```
