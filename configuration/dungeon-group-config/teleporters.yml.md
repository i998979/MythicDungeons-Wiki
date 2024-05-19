# teleporters.yml

```yaml
# Teleporters that players can shift on it and teleport to designated location
Teleporters:
  # ID of the teleporter, must be unique
  '1':
    Name: '&bMountain'
    Location:
      world: dungeon
      x: 124.5
      y: 5.0
      z: 262.5
    Range: 1.5
    Effects:
      # Appear when the teleporter is not used
      Idle:
        - vortex 3.0
      # Appear when the teleporter is teleporting players
      Teleporting:
        - vortex 3.0
      # Appear when the teleporter is in cooldown
      Cooldown:
        - vortex 3.0
    Hologram:
      Idle:
        Offset: 4.0
        Lines:
          - '&bTELEPORT TO'
          - '&f&lMOUNTAIN'
          - '&f&l!TELEPORT!'
          - '{material=WHITE_WOOL}'
      Teleporting:
        Offset: 2.0
        Lines:
          - '&bTELEPORT TO'
          - '&f&lMOUNTAIN'
          - 'Teleport in %time%s'
          - '{material=WHITE_WOOL}'
      Cooldown:
        Offset: 6.0
        Lines:
          - '&bTELEPORT TO'
          - '&f&lMOUNTAIN'
          - 'Cooldown in %cooldown%s'
          - '{material=WHITE_WOOL}'
    # Destination of the teleporter
    Destination:
      world: dungeon
      x: 120.5
      y: 5.0
      z: 256.5
      pitch: 0.0
      yaw: 0.0
    # How long(in ticks) the player required to stay in the teleporter before getting teleported
    Time: 60
    # Cooldown of the teleporter before it can be used again
    Cooldown: 60
```
