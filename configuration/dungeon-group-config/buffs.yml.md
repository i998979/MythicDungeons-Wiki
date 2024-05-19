# buffs.yml

```yaml
# Buffs that players can get potion effects
Buffs:
  # ID of the buff, must be unique
  '1':
    # Name of the buff
    Name: '&b&lSPEED BOOST'
    # Location of the buff
    Location:
      world: dungeon
      x: 120.5
      y: 5.0
      z: 262.5
    # How big is the buff
    Range: 3.0
    # Particle effects of the buff, only effects declared in "effects.yml" can be used
    Effects:
      # Appear when the buff is not claimed
      Idle:
        - vortex 3.0
      # Appear when the buff is being claimed
      Claiming:
        - vortex 4.0
      # Appear when the buff is in cooldown
      Cooldown:
        - vortex 2.0
    Hologram:
      Idle:
        # Vertical offset of the hologram based on the original location
        Offset: 3.0
        Lines:
          - '{material=PLAYER_HEAD;glow=true;damage=0;skullowner=991d961c-b6b4-4d49-88e6-01788cf445dc}'
          - '0 &fCLAIM ME!'
      Claiming:
        Offset: 4.0
        Lines:
          - '{material=PLAYER_HEAD;glow=true;damage=0;skullowner=3fb398fb-f50a-42de-998d-692c35048e86}'
          - '1 &7CLAIMING in %time%'
      Cooldown:
        Offset: 2.0
        Lines:
          - '{material=PLAYER_HEAD;glow=true;damage=0;skullowner=34a35801-3895-4aae-a7e5-fbb52e575e3d}'
          - '2 &7CLAIMABLE in %cooldown%'
    # Potion effects to apply
    # Check here for available potion effects name
    # https://hub.spigotmc.org/javadocs/spigot/org/bukkit/potion/PotionEffectType.html
    # - PotionType Duration(in ticks) Amplifier Ambient Particles Icon
    Potions:
      - SPEED 10 2 true true true
    # Type of the buff
    # ONETIME: The buff can only be claimed once
    # REPEAT=<tick>: The buff can be claimable again after <tick> ticks
    Type: REPEAT=20
    # How long(in ticks) the player required to stay before the buff is being claimed
    Time: 60
    # If true, when the player claimed the buff, others can still claim the buff
    # If false, when the player claimed the buff, others cannot claim the buff
    PerPlayer: true
    # If true, the effects are applied to all team members
    # If false, the effects are applied to the claimed player only
    ToTeam: true
```
