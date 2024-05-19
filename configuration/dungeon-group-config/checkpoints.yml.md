# checkpoints.yml

```yaml
# Checkpoints that players required to reach when necessary
Checkpoints:
  # ID of the checkpoint, must be unique
  '1':
    # Name of the checkpoint
    Name: '&bMountain'
    # Single-point checkpoint, it will be captured if the player stays within range
    Location:
      world: dungeon
      x: 116.0
      y: 5.0
      z: 262.0
    # Regional checkpoint, it will be captured if the player stays between 2 points
    # Regions:
    #   Min:
    #     world: dungeon
    #     x: 114.5
    #     y: 0.0
    #     z: 264.5
    #   Max:
    #     world: dungeon
    #     x: 117.5
    #     y: 256.0
    #     z: 261.5
    # Multi-point checkpoint, it will be captured if the player stays within range of either point
    # Or players are required to stay in all points
    # Points:
    #   '0':
    #     world: dungeon
    #     x: 115.0
    #     y: 5.0
    #     z: 262.0
    #   '1':
    #     world: dungeon
    #     x: 116.0
    #     y: 5.0
    #     z: 262.0
    #   '2':
    #     world: dungeon
    #     x: 117.0
    #     y: 5.0
    #     z: 262.0
    # Particle effects of the checkpoint, only effects declared in "effects.yml" can be used
    # How big is the checkpoint
    Range: 3.0
    Effects:
      # Appear when the checkpoint is not claimed
      Idle:
        - vortex 3.0
      # Appear when the checkpoint is being claimed
      Claiming:
        - vortex 3.0
      # Appear when the checkpoint is claimed
      Claimed:
        - vortex 3.0
    Hologram:
      Idle:
        # Vertical offset of the hologram based on the original location
        Offset: 4.0
        Lines:
          - '{material=PLAYER_HEAD;glow=true;damage=0;skullowner=991d961c-b6b4-4d49-88e6-01788cf445dc}'
          - '0 &bMountain'
          - '0 &fThe coldest point that'
          - '0 '
          - '0 &fno one has been here before'
      Claiming:
        Offset: 6.0
        Lines:
          - '{material=PLAYER_HEAD;glow=true;damage=0;skullowner=3fb398fb-f50a-42de-998d-692c35048e86}'
          - '1 &bMountain'
          - '1 &fThe coldest point that'
          - '1 &fno one has been here before'
          - '1 Claiming in %time%s'
      Claimed:
        Offset: 2.0
        Lines:
          - '{material=PLAYER_HEAD;glow=true;damage=0;skullowner=34a35801-3895-4aae-a7e5-fbb52e575e3d}'
          - '2 &bMountain'
          - '2 &fThe coldest point that'
          - '2 &fno one has been here before'
          - '2 Claimed'
    # Spawnpoint of the checkpoint, the player respawns in the list of locations if configured
    Spawnpoints:
      '0':
        world: dungeon
        x: 115.0
        y: 5.0
        z: 262.0
        pitch: 0.0
        yaw: 0.0
      '1':
        world: dungeon
        x: 116.0
        y: 5.0
        z: 262.0
        pitch: 0.0
        yaw: 0.0
      '2':
        world: dungeon
        x: 116.0
        y: 5.0
        z: 263.0
        pitch: 0.0
        yaw: 0.0
```
