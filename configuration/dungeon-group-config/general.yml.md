# general.yml

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
