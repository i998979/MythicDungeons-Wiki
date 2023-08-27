# Dungeon Group Config (Simplified)

{% hint style="danger" %}
**Warning:** The sample config is purely for reference only. Do not copy & paste, change the parameters like location, and mob type accordingly.
{% endhint %}

## Dungeon group (Simplified)

Dungeon Group is the type of dungeon, all the dungeon instances share the same arguments. But dungeon-specific arguments like origin, PlayerSpawns are automatically calculated.

In case you are not familiar with the configuration and are confused about configuring the dungeon such as which part is necessary and which part isn't, here is a simplified configuration, only necessary sections are left.

It assumes that you have the default mob `SkeletalKnight` declared in MythicMobs and use world `dungeon` as dungeon world, change accordingly.

This dungeon requires you to kill 1 `SkeletalKnight` within `60` seconds to finish.

{% code title="Ruins.yml" lineNumbers="true" %}
```yaml
# Dungeon Group ID, must be unique and same as the file name
Ruins:
  # General configurations of the dungeon
  General:
    # Display name of the dungeon, it will be shown on GUI, scoreboards and messages
    Name: '&4Ruins'
    # Minimum players required for the dungeon
    MinPlayer: 1
    # Maximum players allowed for the dungeon
    MaxPlayer: 4
    # Location where the dungeon schematic will start to place
    # It should be the lower corner of the dungeon
    Origin:
      world: dungeon
      x: 127.0
      y: 4.0
      z: 245.0
    # Icon of this Dungeon Group in Dungeon Type Selector
    # Use "/mg check" with the items on your hand to retrieve the string
    Icon: '{"v":2865,"type":"REDSTONE_BLOCK"}'
  # How the dungeon is placed
  Map:
    # Length, Width, Height are optional if you have dungeon schematic in place
    # All length, width, and height must be configured in order to work
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
  # How long is the dungeon challenge time, what to do after it ends
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
  # Main flow of the dungeon
  Stages:
    # ID of the stage, must be unique
    '0':
      Options:
        # True if this is the first stage of the dungeon, only 1 can be existed
        Initial: true
        # True if this is the last stage of the dungeon, more than 1 can be existed
        End: true
      # A list of actions will do when this stage starts
      Actions:
        - MythicMob{type=SkeletalKnight;at=LOCATION;world=dungeon;x=1160.5;y=5.5;z=252.0;yaw=0.0;pitch=0.0}
      # A list of objectives need to be fulfilled to complete this stage
      Objectives:
        - MythicMob{type=SkeletalKnight;amount=1}
      # A list of actions will do when this stage is completed
      Completions: [ ]
      # A list of actions will do when the dungeon is failed during this stage
      FailActions: [ ]
      # A list of stages that will start when this stage is completed
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
```
{% endcode %}
