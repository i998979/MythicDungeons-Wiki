# Scoreboards

{% hint style="info" %}
**Reminder:** This page might not be updated regularly. You may check the changelog on the resource page or inside the downloaded jar.

Please let me know if you need additional placeholders.
{% endhint %}

## Scoreboard Text (scoreboard.yml)

Available placeholders for specific scoreboard is located below the corresponding scoreboard.

Please keep in mind that `%bosscond%` under `InGame.Scores` are vertically scrolled independently and you should maintain the `Boss`, `AmountToKill`, `MobToKill`, `Checkpoint` and `LootChest` do not exceed the length of the scoreboard.

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
InGame:
  # %expire%: Time before the dungeon expires, and you automatically fail
  # %objective%: Reserved space to display boss-related status messages
  Interval: 10
  Title:
    - "&6&lMythicDungeons"
    - "&eMythicDungeons"
  # If the %objective%'s information size doesn't fit the size designated below,
  # how fast will the text scroll
  ScrollInterval: 20
  Scores:
    - "&e&m--------===========--------"
    - "&eDungeon&7: &f%dungeon%"
    - "&eTime left&7: &f%expire%"
    - "&1"
    - "&2%objective%"
    - "&3%objective%"
    - "&4%objective%"
    - "&5%objective%"
    - "&6%objective%"
    - "&7%objective%"
    - "&8%objective%"
    - "&9%objective%"
    - "&0%objective%"
    - "&2"
    - "&ewww.Example.com"
  # Lines between 2 consecutive boss information
  Spaces: 2

  # %block%: Block type required to break
  # %broke%: Blocks broke
  # %amount%: Amount of blocks needed to break
  # %world1% %x1% %y1% %z1%: First corner of the region
  # %world2% %x2% %y2% %z2%: Second corner of the region
  # Break Stone 0/3
  BlockBreak:
    - "&eBreak %block% %broke%/%amount%"
  # Break Stone
  # Cobblestone
  # Gravel 0/3
  BlockBreakCombined:
    - "&eBreak %block%"
    - "&e%block%"
    - "&e%block% %broke%/%amount%"

  # %block%: Block type required to place
  # %placed%: Blocks placed
  # %amount%: Amount of blocks needed to place
  # %world1% %x1% %y1% %z1%: First corner of the region
  # %world2% %x2% %y2% %z2%: Second corner of the region
  # Place Stone 0/3
  BlockPlace:
    - "&ePlace %amount%x %block%"
  # Place Stone
  # Cobblestone
  # Gravel 0/3
  BlockPlaceCombined:
    - "&ePlace %block%"
    - "&e%block%"
    - "&e%block% %placed%/%amount%"

  # %chatscoreboard%: Chat message required, scoreboard text is additionally defined in action
  # %chathassaid%: Is this message has been said by players
  # "Say 123456: Yes"
  ChatMessage: "Say %chatscoreboard%: %chathassaid%"

  # %cp%: Name of the checkpoint needs to be reached
  # %cpreached% Checkpoint reached or not
  # "Mountain: Not reached"
  Checkpoint: "&e%cp%&7: &f%cpreached%"

  # %item%: Display name of the item required, if the item has no display name, material name is shown instead
  # %amount%: Amount of the item required
  # %hasitem%: Does any/all player have all required items or not
  # "Has 1x REDSTONE_BLOCK: Yes"
  HasItem: "&eHas %amount%x %item%&7: &f%hasitem%"
  # "Has 1x REDSTONE_BLOCK"
  # "or 1x DIAMOND_BLOCK"
  # "or 1x GOLD_BLOCK: Yes"
  HasItemMultiple:
    - "&eHas %amount%x %item%"
    - "&eor %amount%x %item%"
    - "&eor %amount%x %item%&7: &f%hasitem%"

  # %lc%: Name of the loot chest needs to be opened
  # %lcopened% Lootchest opened or not
  # "Treasure: Not opened"
  LootChest: "&e%lc%&7: &f%lcopened%"

  # %mobamtkill%: Mob that requires certain amount of kills
  # %mobamtmax%: Amount of mob that players need to kill
  # %mobminlevel%: Minimum level of mob that players need to kill
  # %mobmaxlevel%: Maximum level of mob that players need to kill
  # %mobamtkilled%: Amount of mob killed
  # "Lv1 Rat: 3/5"
  AmountToKill: "&eLvl %mobminlevel%-%mobmaxlevel% %mobamtkill%&7: &f%mobamtkilled%/%mobamtmax%"

  # %mobkill%: Mob that has to be killed
  # %mobkilled%: Mob dead or not
  # "Mother rat: Killed"
  MobToKill: "&e%mobkill%&7: &f%mobkilled%"

  # %npcname%: Name of the NPC
  # %npcinteract%: Left click, Right click or both accepted
  # %npcinteracted%: Did the player interact with NPC or not
  # Click NPC1: Yes
  NPCInteract: "%e%npcinteract% %npcname%&7: %npcinteracted%"

  # %item%: Item required player to pick up
  # %picked%: Is the item picked up or not
  # "Picked up REDSTONE_BLOCK: Yes"
  PlayerPickup: "&ePicked up %item%&7: %picked%"
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
