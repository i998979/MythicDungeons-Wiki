# Dungeon Group Config (Full)

{% hint style="danger" %}
**Warning:** The sample config is purely for reference only. Do not copy & paste, change the parameters like location, and mob type accordingly.
{% endhint %}

## Dungeon Group (Full)

If you are familiar with the configuration, here is a full configuration.

{% code title="Ruins.yml" lineNumbers="true" %}
```yaml
# Dungeon Group ID, must be unique and same as the file name
Ruins:
  # General configurations of the dungeon
  General:
    # Display Name of the dungeon, it will be shown on GUI, scoreboards and messages
    Name: '&4Ruins'
    # Minimum players required for the dungeon
    MinPlayer: 1
    # Maximum players allowed for the dungeon
    MaxPlayer: 4
    # Are players visible to other challengers in the same Dungeon Group except for their teammates
    VisibleToNearby: false
    # Death limits before the player fails the dungeon
    # Available limits:
    # none: No limit
    # team 10: 10 deaths total for the whole team
    # player 3: 3 deaths total for any 1 player
    DeathLimit: none
    # Death Penalty when the player dies
    DeathPenalty:
      # Use player's death or team's death for counting
      PerPlayer: true
      # Item penalty
      Items:
        Enabled: true
        Items:
          # Death count, different death counts drop different lists of items
          # If the player dies once, an Emerald Block and items drawn from LootTable will be removed from the player's inventory/death drop
          # If '3' is enabled and the player dies twice, items in '1' will be removed
          '1':
            - '{"v":2865,"type":"EMERALD_BLOCK"}'
            - 'LootTable{id=Stage1Table}'
          # If the player dies 3 times, a Diamond Block will be removed from the player's inventory/death drop
          # '3':
          #   - '{"v":2865,"type":"DIAMOND_BLOCK"}'
      # Money penalty. Only effective if Vault and economy plugin is installed and the hook is enabled
      Money:
        Enabled: true
        Amount:
          '1': 300
    # Inventory items will not drop on the ground upon death
    KeepInventory: true
    # Experience will not drop on the ground upon death
    KeepExperience: true
    # Additional title countdown, players will be invincible and frozen during countdown
    TitleCountdown: false
    # Location where the dungeon schematic will start to place
    # It should be the lower corner of the dungeon
    Origin:
      world: dungeon
      x: 127.0
      y: 4.0
      z: 245.0
    # Icon of this Dungeon Group in Dungeon Type Selector
    # Either use "/mg check" with the items on your hand to retrieve the string
    # Or follow the format in menu.yml
    # The dungeon will be sorted by the time it is loaded if only 1 is specified
    Icon: '{"v":2865,"type":"REDSTONE_BLOCK"}'
    # If the slot is specified, it will be placed in that slot
    # All existing buttons will be overridden
    # If the slot is not specified, it will be placed in the next available slot
    # Icon:
    #   Items:
    #     - '{"v":2865,"type":"REDSTONE_BLOCK"} 0'
    #     - '{"v":2865,"type":"REDSTONE_BLOCK"} 1'
    #     - '{"v":2865,"type":"REDSTONE_BLOCK"} 2'
    # Blacklist items that cannot be brought into the dungeon
    BlacklistItems:
      - '{"v":2865,"type":"EMERALD_BLOCK"}'
      - 'LootTable{id=Stage1Table}'
    # Signs for users to click to join/leave the dungeon queue (temporary room)
    Signs:
      # Enable/disable all signs
      Enabled: true
      # Configure Join Signs
      Join:
        # Location of the Join Signs, ID must be unique
        Locations:
          '0':
            world: dungeon
            x: 113.0
            y: 4.0
            z: 242.0
      Leave:
        # Configure Leave Signs
        Locations:
          # Location of the Leave Signs, ID must be unique
          '0':
            world: dungeon
            x: 112.0
            y: 4.0
            z: 242.0
    # Citizens NPCs for users to click to join/leave the dungeon queue (temporary room)
    # All NPCs must be configured and spawned in the world by Citizens
    NPCs:
      # Enable/disable all NPCs
      Enabled: true
      # Configure Join NPCs
      Join:
        # ID of the NPCs in Citizens
        IDs:
          - 0
          - 1
      # Configure Leave NPCs
      Leave:
        IDs:
          - 2
          - 3
  # The cost of starting the dungeon
  Price:
    # Money to pay to start the dungeon
    Money:
      # Pay money or not. Only effective if Vault and economy plugin is installed and the hook is enabled
      Use: true
      # Deduct per player, if you have 3 players, all of them pay 30000.0
      # Otherwise, only the leader will be charged
      PerPlayer: true
      # Amount to charge
      Amount: 30000.0
    # Items to pay to start the dungeon
    Items:
      # Pay items or not
      Use: true
      # Deduct per player, the items in the list will be removed from all players
      # Otherwise, only the leader will be charged
      PerPlayer: true
      # Items to pay
      # Some custom item plugins are supported, DO NOT add extra spaces or quotations
      # Only Loot Tables declared in "loottables" folder are supported
      # Use "/mg check" with the items on your hand to retrieve the string
      Items:
        - "{\"v\":3578,\"type\":\"DIAMOND_BLOCK\"}"
        - "{\"v\":3578,\"type\":\"REDSTONE_BLOCK\"}"
        - "{\"v\":3578,\"type\":\"EMERALD_BLOCK\"}"
        # - 'MMOItems{type=FOOD;id=ICE_CREAM;amount=64}'
        # - 'MythicMobs{id="SkeletonKingSword";amount=2}'
        # - 'ItemsAdder{id=iron_search;amount=2}'
        # - 'EcoItems{id=armor_core;amount=1}'
        # - 'EcoArmor{id=default;amount=1;type=crystal}'
        # - 'EcoArmor{id=reaper;amount=1;type=set;slot=boots}'
        # - 'EcoArmor{id=reaper;amount=1;type=shard}'
        # - 'Talismans{id=boss_1;amount=1}'
        # - 'LootTable{id=Stage1Table}'
  # How the dungeon is placed
  Map:
    # Length, Width, Height are optional if you have a dungeon schematic in place
    # All length, width, and height must be configured to work
    # Otherwise it will still be automatically calculated depending on the schematic
    #
    # Length of the dungeon, spanned on z-axis positive
    # Use negative value in Width and ColumnGap if you want z-axis spans in the opposite direction
    # Length: 19
    # Width of the dungeon, spanned on x-axis positive
    # Use negative value in Length and RowGap if you want x-axis spans in the opposite direction
    # Width: 13
    # Height of the dungeon, spanned on y-axis positive
    # Height: 7
    # How many rows will be placed, the total amount of dungeon is "row * column"
    Row: 3
    # How many blocks of the gap in rows between adjoining dungeons
    RowGap: 1
    # How many columns will be placed, the total amount of dungeon is "row * column"
    Column: 3
    # How many blocks of the gap in columns between adjoining dungeons
    ColumnGap: 1
  # How long is the dungeon challenge time, and what to do after it ends
  Expire:
    # Maximum dungeon challenge time(in sec), after the timer ends, the dungeon fails
    Time: 60
    # Time before teleporting players back(in sec)
    Teleport: 10
    # Where to teleport after the dungeon ends
    # Available location:
    # DESIGNATED: Designated location
    # PREVIOUS: Player's previous location
    TeleportTo: DESIGNATED
    # Designated location when "TeleportTo" is "DESIGNATED"
    Designated:
      world: dungeon
      x: 109.5
      y: 5.0
      z: 242.5
      pitch: 180.0
      yaw: 0.0
  # Main flow of the dungeon
  Stages:
    # ID of the stage, must be unique
    '0':
      Options:
        # True if this is the first stage of the dungeon, only 1 can exist
        Initial: true
      # A list of actions will do when this stage starts
      Actions:
        - MythicSpawner{type=rat1;world=dungeon;x=116.0;y=5.0;z=255.0;yaw=0.0;pitch=0.0;settings=rat1.yml}
        - MythicSpawner{type=rat1;world=dungeon;x=116.0;y=5.0;z=252.0;yaw=0.0;pitch=0.0;settings=rat1.yml}
        - MythicSpawner{type=rat2;world=dungeon;x=124.0;y=5.0;z=252.0;yaw=0.0;pitch=0.0;settings=rat2.yml}
      # A list of objectives needs to be fulfilled to complete this stage
      Objectives:
        - MythicMob{type=rat1;amount=3}
        - Checkpoint{id=1}
      # A list of actions will do when this stage is completed
      Completions: [ ]
      # A list of actions will do when the dungeon fails during this stage
      FailActions: [ ]
      # A list of stages that will start when this stage is completed
      Branches:
        - Branch{id=1}
    '1':
      Options:
        # How long(in ticks) before this stage starts
        Delay: 20
      Actions:
        - MythicMob{type=rat3;at=LOCATION;world=dungeon;x=120.5;y=5.0;z=259.5;yaw=180.0;pitch=0.0}
      Objectives:
        - MythicMob{type=rat2;amount=2}
        - MythicMob{type=rat3}
      Completions: [ ]
      FailActions: [ ]
      Branches:
        - Branch{id=2}
    '2':
      Options:
        # True if this is the last stage of the dungeon, more than 1 can exist
        End: true
      Actions:
        - MythicMob{type=rat4;at=NEARBY;radius=10.0}
      Objectives:
        - MythicMob{type=rat4}
      Completions:
        - Message{text='&d&lIMPRESSIVE, you have completed the challenge, you may now leave.'}
      FailActions: [ ]
      Branches: [ ]
  # Spawn/Respawn point of the players, they will be randomly teleported to the locations in the list
  PlayerSpawns:
    '0':
      world: dungeon
      x: 121.47342204269181
      y: 5.0
      z: 247.30001128668135
      pitch: 0.0
      yaw: 0.0
    '1':
      world: dungeon
      x: 120.49530775493284
      y: 5.0
      z: 248.4028314339493
      pitch: 0.0
      yaw: 0.0
    '2':
      world: dungeon
      x: 119.51566596838329
      y: 5.0
      z: 247.53789380317693
      pitch: 0.0
      yaw: 0.0
  # Buffs that players can get potion effects
  Buffs:
    '1':
      # Name of the buff
      Name: '&b&lSPEED BOOST'
      # Location of the buff
      Location:
        world: dungeon
        x: 120.5
        y: 5.0
        z: 262.5
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
      # How big is the buff
      Range: 3.0
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
  # Checkpoints declaration so that it can be used in stages
  Checkpoints:
    '1':
      Name: '&bMountain'
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
      Range: 3.0
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
      # Spawnpoint of the checkpoint, the player respawns in the list of locations after death if configured
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
  # Loot chests that players can get items from it
  LootChests:
    '1':
      Name: "&eTreasure Chest"
      # Location of the loot chest
      Location:
        world: dungeon
        x: 125.0
        y: 5.0
        z: 260.0
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
  # Teleporters that players can shift on it and teleport to designated location
  Teleporters:
    '1':
      Name: '&bMountain'
      Location:
        world: dungeon
        x: 124.5
        y: 5.0
        z: 262.5
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
      Range: 1.5
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
  # Rewards that will be given to players when the dungeon is completed
  Rewards:
    # Team reward
    Teams:
      # Guaranteed rewards
      Guaranteed:
        DiamondBlockAndApplePieAndSomeMoney:
          # Money to give
          Money: 30001.0
          # Items to give
          # Some custom item plugins are supported, DO NOT add extra spaces or quotations
          # Only Loot Tables declared in "loottables" folder are supported
          # Use "/mg check" with the items on your hand to retrieve the string
          Items:
            - '{"v":2865,"type":"DIAMOND_BLOCK"}'
          # Commands that will be executed for all players
          Commands:
            # Available placeholders:
            # %player%: The player that gets the reward
            - '{ from=CONSOLE;command=''mi give FOOD APPLE_PIE %player%'' }'
            # Corresponding permissions are required if needed for players to run the command
            - '{ from=PLAYER;command=''me has just rewarded an apple pie!'' }'
      # Weighted rewards
      Weighted:
        CrazyRare:
          # Drop chance of this reward
          # Chances are weightings. For example, "Rare" has a 50 chance
          # Total chance will be 30 + 50 = 80
          # The chance of dropping "CrazyRare" will be 30 / 80 = 37.5%
          Chance: 30
          Items:
            - '{"v":2865,"type":"REDSTONE_BLOCK"}'
            - '{"v":2865,"type":"GOLD_BLOCK"}'
          Commands: [ ]
        # Rare:
        #   Chance: 50
        #   Items:
        #     - '{"v":2865,"type":"REDSTONE_BLOCK"}'
        #     - '{"v":2865,"type":"GOLD_BLOCK"}'

```
{% endcode %}
