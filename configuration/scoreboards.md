# Scoreboards

{% hint style="info" %}
**Reminder:** This page might not be updated regularly. You may check the changelog on the resource page or inside the downloaded jar.

Please let me know if you need additional placeholders.
{% endhint %}

## Scoreboard Text (scoreboard.yml)

Available placeholders for specific scoreboard are located below the corresponding scoreboard.

Due to Minecraft's limitation, at most 16 lines can be displayed on scoreboard, exceeding lines will not be shown.

Since 3.1.0-BETA, Right Text (line numbers) will be hidden automatically. Right Text can be configured by splitting the line with `||`  and it will be split automatically.

{% code title="scoreboard.yml" lineNumbers="true" %}
```yaml
InRoom:
  # Scoreboard display when player is in a room
  # %id%: Room's ID
  # %dungeon%: Room's dungeon group
  # %owner%: Room's owner
  # %current%: Room's member count
  # %min%: Room's min member
  # %max%: Room's max member
  # %note%: Room's note
  # %privacy%: Room's privacy
  # %password%: Room's password
  # %created%: Room's creation time
  # %visible%: Room's visibility in menu
  # %status%: Room's status
  Owner:
    Interval: 10
    Title:
      - "&6&lMythicDungeons"
      - "&eMythicDungeons"
    Scores:
      - "&0"
      - "&eDungeon||&f%dungeon%"
      - "&1"
      - "&eStatus||&f%status%"
      - "&2"
      - "&ePlayers||&f%current%/%max%"
      - "&3"
      - "&eID||&f%id%"
  Member:
    Interval: 10
    Title:
      - "&6&lMythicDungeons"
      - "&eMythicDungeons"
    Scores:
      - "&0"
      - "&eDungeon||&f%dungeon%"
      - "&1"
      - "&eStatus||&f%status%"
      - "&2"
      - "&ePlayers||&f%current%/%max%"
      - "&3"
      - "&eOwner||&f%owner%"
  NoOwner:
    Interval: 10
    Title:
      - "&6&lMythicDungeons"
      - "&eMythicDungeons"
    Scores:
      - "&0"
      - "&eDungeon||&f%dungeon%"
      - "&1"
      - "&eStatus||&f%status%"
      - "&2"
      - "&ePlayers||&f%current%/%max%"
Starting:
  # Scoreboard display when owner starts the dungeon
  # %id%: Room's ID
  # %dungeon%: Room's dungeon group
  # %owner%: Room's owner
  # %current%: Room's member count
  # %min%: Room's min member
  # %max%: Room's max member
  # %note%: Room's note
  # %privacy%: Room's privacy
  # %password%: Room's password
  # %creation%: Room's creation time
  # %visible%: Room's visibility in menu
  # %status%: Room's status
  Owner:
    Interval: 10
    Title:
      - "&6&lMythicDungeons"
      - "&eMythicDungeons"
    Scores:
      - "&0"
      - "&eDungeon||&f%dungeon%"
      - "&1"
      - "&eStatus||&f%status%"
      - "&2"
      - "&ePlayers||&f%current%/%max%"
      - "&3"
      - "&eID||&f%id%"
  Member:
    Interval: 10
    Title:
      - "&6&lMythicDungeons"
      - "&eMythicDungeons"
    Scores:
      - "&0"
      - "&eDungeon||&f%dungeon%"
      - "&1"
      - "&eStatus||&f%status%"
      - "&2"
      - "&ePlayers||&f%current%/%max%"
      - "&3"
      - "&eOwner||&f%owner%"
Ending:
  # %dungeon%: Dungeon's name
  # %teleport%: Time before dungeon ends and teleport all challengers to lobby
  Interval: 10
  Title:
    - "&6&lMythicDungeons"
    - "&eMythicDungeons"
  Scores:
    - "&0"
    - "&eDungeon||&f%dungeon%"
    - "&1"
    - "&eTeleport in||&f%teleport%"
    - "&2"
    - "&3"
    - "&4"
    - "&5"

```
{% endcode %}
