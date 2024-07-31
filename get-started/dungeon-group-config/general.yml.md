# general.yml

## General Config (Simplified)

```yaml
# General configurations of the dungeon
General:
  # Display Name of the dungeon, it will be shown on GUI, scoreboards and messages
  Name: '&4Ruins'
  # Minimum players required for the dungeon
  MinPlayer: 1
  # Maximum players allowed for the dungeon
  MaxPlayer: 4
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
# How the dungeon is placed
Map:
  # Name of the schematic to place
  Schematic: Ruins.schem
  # Location where the dungeon schematic will start to place
  # It should be the lower corner of the dungeon
  Origin:
    world: dungeon
    x: 127.0
    y: 4.0
    z: 245.0
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
  TeleportTo: PREVIOUS
# Spawn/Respawn point of the players, they will be randomly teleported to the locations in the list
PlayerSpawns:
  '0':
    world: dungeon
    x: 121.47342204269181
    y: 5.0
    z: 247.30001128668135
    pitch: 0.0
    yaw: 0.0

```

## General Config (Full)

```yaml
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
  # Show message to remind player the dungeon is about to end, ascending order, in seconds
  PlaytimeRemind: '60 30 15 5'
  # How long will the dungeon start if the room has enough players, only effective when joining through signs or NPCs
  AutoStartTimer: 30
  # Show message to remind player the dungeon is about to auto-start, ascending order, in seconds
  AutoStartTimeRemind: '60 30 15 5'
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
      Items:
        # Death count, different death counts drop different lists of items
        # If the player dies once, an Emerald Block and items drawn from LootTable will be removed from the player's inventory/death drop
        # If '3' is enabled and the player dies twice, items in '1' will be removed
        '0':
          - '{"v":2865,"type":"EMERALD_BLOCK"}'
          - 'LootTable{id=Stage1Table}'
        # If the player dies 3 times, a Diamond Block will be removed from the player's inventory/death drop
        # '3':
        #   - '{"v":2865,"type":"DIAMOND_BLOCK"}'
    # Money penalty. Only effective if Vault and economy plugin is installed and the hook is enabled
    Money:
      Amount:
        '1': 300
  # Cancel death screen when the player dies
  AutoRespawn: true
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
  # Inventory items will not drop on the ground upon death
  KeepInventory: true
  # Experience will not drop on the ground upon death
  KeepExperience: true
  # Potion effects will be saved and removed in the dungeon and revert after dungeon ends
  KeepPotions: true
  # Allow breaking blocks in the dungeon, not including specified blocks in a specified location
  BlockBreak: true
  # Allow placing blocks in the dungeon, not including specified blocks in a specified location
  BlockPlace: true
  # Allow interacting blocks in the dungeon, not including specified blocks in a specified location
  BlockInteract: true
  # Block PvP when challenging dungeon
  BlockPvP: true
  # Block commands when challenging dungeon
  BlockCommands: true
  # Command whitelist while BlockCommands is enabled
  # All MythicDungeons commands are whitelisted by default
  Whitelist: [ ]
  # Whitelist:
  # - heal
  # - kill
  # Hide messages sent by dungeon challengers from all players
  # Hide messages sent by all players except teammates from dungeon challengers
  HideOtherChat: false
  # Use countdown GUI to allow cancelling pre-starting dungeon
  GUICountdown: false
  # Additional title countdown, players will be invincible and frozen during countdown
  TitleCountdown: false
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
Requirements:
  Permission: true
  # Money to pay to start the dungeon
  Money:
    # Deduct per player, if you have 3 players, all of them pay 30000.0
    # Otherwise, only the leader will be charged
    PerPlayer: true
    # Amount to charge
    Amount: 30000.0
  # Items to pay to start the dungeon
  Items:
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
  Conditions:
    Required:
      - '%changeoutput_>=_input:{player_level}_matcher:5_ifmatch:true_else:false% true'
    Optional:
      - '%changeoutput_ignorecase_input:{player_allow_flight}_matcher:yes_ifmatch:true_else:false% true'
      - '%changeoutput_>=_input:{player_exp}_matcher:1_ifmatch:true_else:false% true'
# How the dungeon is placed
Map:
  # Name of the schematic to place
  Schematic: Ruins.schem
  # Location where the dungeon schematic will start to place
  # It should be the lower corner of the dungeon
  Origin:
    world: dungeon
    x: 127.0
    y: 4.0
    z: 245.0
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
  # Restore the dungeon to what it used to look like after the challenge is ended
  RestoreTerrains: true
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
