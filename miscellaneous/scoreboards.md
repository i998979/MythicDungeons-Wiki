# Scoreboards

{% hint style="info" %}
**Reminder:** This page might not be updated regularly. You may check the changelog on the resource page or inside the downloaded jar.

Please let me know if you need additional placeholders.
{% endhint %}

## Scoreboard Text (scoreboard.yml)

Available placeholders for specific scoreboard is located below the corresponding scoreboard.

~~Please keep in mind that `%bosscond%` under `InGame.Scores` are vertically scrolled independently and you should maintain the `Boss`, `AmountToKill`, `MobToKill`, `Checkpoint` and `LootChest` do not exceed the length of the scoreboard.~~

{% code title="scoreboard.yml" lineNumbers="true" %}
```yaml
InRoom:
  # Scoreboard display when player is in a room
  # %id%: Room's id
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
      - "&e&m--------===========--------"
      - "&eDungeon&7: &f%dungeon%"
      - "&1"
      - "&eStatus: &f%status%"
      - "&2"
      - "&ePlayers: &f%current%/%max%"
      - "&3"
      - "&eId: &f%id%"
      - "&4"
      - "&ewww.Example.com"
  Member:
    Interval: 10
    Title:
      - "&6&lMythicDungeons"
      - "&eMythicDungeons"
    Scores:
      - "&e&m--------===========--------"
      - "&eDungeon&7: &f%dungeon%"
      - "&1"
      - "&eStatus: &f%status%"
      - "&2"
      - "&ePlayers: &f%current%/%max%"
      - "&3"
      - "&eOwner: &f%owner%"
      - "&4"
      - "&ewww.Example.com"
  NoOwner:
    Interval: 10
    Title:
      - "&6&lMythicDungeons"
      - "&eMythicDungeons"
    Scores:
      - "&e&m--------===========--------"
      - "&eDungeon&7: &f%dungeon%"
      - "&1"
      - "&eStatus: &f%status%"
      - "&2"
      - "&ePlayers: &f%current%/%max%"
      - "&3"
      - "&ewww.Example.com"
Starting:
  # Scoreboard display when owner starts the dungeon
  # %id%: Room's id
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
      - "&e&m--------===========--------"
      - "&eDungeon&7: &f%dungeon%"
      - "&1"
      - "&eStatus: &f%status%"
      - "&cClick \"Cancel\" to cancel"
      - "&2"
      - "&ePlayers: &f%current%/%max%"
      - "&3"
      - "&eId: &f%id%"
      - "&4"
      - "&ewww.Example.com"
  Member:
    Interval: 10
    Title:
      - "&6&lMythicDungeons"
      - "&eMythicDungeons"
    Scores:
      - "&e&m--------===========--------"
      - "&eDungeon&7: &f%dungeon%"
      - "&1"
      - "&eStatus: &f%status%"
      - "&2"
      - "&ePlayers: &f%current%/%max%"
      - "&3"
      - "&eOwner: &f%owner%"
      - "&4"
      - "&ewww.Example.com"
Ending:
  # %dungeon%: Dungeon's name
  # %teleport%: Time before dungeon ends and teleport all challengers to lobby
  Interval: 10
  Title:
    - "&6&lMythicDungeons"
    - "&eMythicDungeons"
  Scores:
    - "&e&m--------===========--------"
    - "&eDungeon&7: &f%dungeon%"
    - "&eTeleport in &f%teleport%"
    - "&1"
    - "&2"
    - "&3"
    - "&4"
    - "&5"
    - "&6"
    - "&7"
    - "&8"
    - "&9"
    - "&0"
    - "&a"
    - "&ewww.Example.com"
```
{% endcode %}
