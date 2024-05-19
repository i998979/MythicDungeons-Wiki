# traps.yml

```yaml
# Different types of traps that can damage players
Traps:
  # Arrow trap that shoots arrows
  Arrow:
    # ID of the trap, must be unique for all traps
    '1':
      # Interval(in ticks) between arrow shoots
      Interval: 20
      # Arrow's damage, 2 means a full heart
      Damage: 5.0
      # How far will the arrow shoot, default dispenser is 1.0
      Velocity: 2.0
      # How long(in ticks) will the player be set on fire when he gets hit
      FireTicks: 60
      Potions:
        - SLOW 10 2 true true true
        - WEAKNESS 2 2 true true true
      # Location of the arrow trap, the block in this location MUST be a dispenser
      Location:
        world: dungeon
        x: 125.0
        y: 5.0
        z: 255.0
    '2':
      Interval: 20
      Damage: 5.0
      Velocity: 1.0
      FireTicks: 60
      Potions:
        - SLOW 10 2 true true true
        - WEAKNESS 2 2 true true true
      Location:
        world: dungeon
        x: 125.0
        y: 5.0
        z: 256.0
    '3':
      Interval: 20
      Damage: 5.0
      Velocity: 1.0
      FireTicks: 60
      Potions:
        - SLOW 10 2 true true true
        - WEAKNESS 2 2 true true true
      Location:
        world: dungeon
        x: 125.0
        y: 5.0
        z: 257.0
  # Damage trap that damages players when they are inside
  Damage:
    '4':
      # Interval(in ticks) between damages
      Interval: 5
      Damage: 2.0
      # First corner of the trap, players staying in this region will be constantly damaged
      Min:
        world: dungeon
        x: 125.0
        y: 5.0
        z: 247.0
      # Second corner of the trap
      Max:
        world: dungeon
        x: 123.0
        y: 5.0
        z: 250.0
  # Fire trap that sets players on fire when they are inside
  Fire:
    '5':
      Damage: 2.0
      # How long(in ticks) will the player be set on fire
      FireTicks: 60
      # Duration(in ticks) of the particles and the interval(in ticks) of it
      # 10 10 20 10 40 10 means the particle spawns for 10, 20, 40 ticks and 10 ticks between them
      Count: 10 10 20 10 40 10
      # Particle effects to apply
      # Check here for available particle effects name
      # https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Particle.html
      # - ParticleType xOffset yOffset zOffset ExtraData
      Particle: FLAME 0.0 0.0 0.0 0.0
      Min:
        world: dungeon
        x: 125.0
        y: 5.0
        z: 247.0
      Max:
        world: dungeon
        x: 123.0
        y: 5.0
        z: 250.0
```
