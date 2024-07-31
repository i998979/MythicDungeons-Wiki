# Displays

`Displays` are used to display objectives in the stage, there are multiple ways to display stage objectives including scoreboard, boss bar, and action bar.

All objectives in the `Displays` follow the order of declared `Objectives` starting from 1.

For example, if stage objectives are declared like this:

```yaml
- MythicMob{type=rat1;amount=3}
- Checkpoint{id=1}
```

The order of Display objectives will be:

```yaml
- '&fSlain %MythicMob_1_mobamtkilled%/%MythicMob_1_mobamtmax%x %MythicMob_1_mobamtkill%'
- '&fDiscover the secret of %Checkpoint_2_cp%: %Checkpoint_2_cpreached%'
```

## General Parameters

## Placeholders

Placeholders are used within Displays to display objective-specific information. It can be used like `%<objective type>_<objective order>_<placeholder>%`. For example, `%MythicMobs_1_mobamtkill%` shows the mob's name required to kill in [MythicMobs Objective](../objectives/objective-list.md#mythicmob).

| Objective                    | Placeholder        | Explanation                                                                                        |
| ---------------------------- | ------------------ | -------------------------------------------------------------------------------------------------- |
| **BlockBreakObjective**      | broke              | Blocks broke                                                                                       |
|                              | amount             | Amount of blocks needed to break                                                                   |
|                              | block              | Block type required to break                                                                       |
|                              | world1, x1, y1, z1 | First corner of the region                                                                         |
|                              | world2, x2, y2, z2 | Second corner of the region                                                                        |
|                              |                    |                                                                                                    |
| **BlockPlaceObjective**      | placed             | Blocks placed                                                                                      |
|                              | amount             | Amount of blocks needed to place                                                                   |
|                              | block              | Block type required to place                                                                       |
|                              | world1, x1, y1, z1 | First corner of the region                                                                         |
|                              | world2, x2, y2, z2 | Second corner of the region                                                                        |
|                              |                    |                                                                                                    |
| **BlockInteractObjective**   | placed             | Block interacted                                                                                   |
|                              | amount             | Amount of blocks needed to interact                                                                |
|                              | block              | Block type required to interact                                                                    |
|                              | world1, x1, y1, z1 | First corner of the region                                                                         |
|                              | world2, x2, y2, z2 | Second corner of the region                                                                        |
|                              |                    |                                                                                                    |
| **BuffClaimObjective**       | bf                 | Buff required to claim                                                                             |
|                              | bfclaimed          | Is this buff claimed                                                                               |
|                              |                    |                                                                                                    |
| **ChatMessageObjective**     | chatscoreboard     | Chat message required, scoreboard text is additionally defined in action                           |
|                              | chathassaid        | Is this message has been said by players                                                           |
|                              |                    |                                                                                                    |
| **CheckpointObjective**      | cp                 | Name of the checkpoint needs to be reached                                                         |
|                              | cpreached          | Checkpoint reached or not                                                                          |
|                              |                    |                                                                                                    |
| **ContainerPickupObjective** | world, x, y, z     | Location of the container                                                                          |
|                              | item               | Item to sacrifice                                                                                  |
|                              | amount             | Amount to sacrifice                                                                                |
|                              | picked             | Is the item picked up by container                                                                 |
|                              |                    |                                                                                                    |
| **DamageObjective**          | damage             | Damage to take                                                                                     |
|                              | time               | Times of the damage to take                                                                        |
|                              | damaged            | Times of the damage taken                                                                          |
|                              |                    |                                                                                                    |
| **HasItemObjective**         | item               | Display name of the item required, if the item has no display name, material name is shown instead |
|                              | amount             | Amount of the item required                                                                        |
|                              | hasitem            | Does any/all player have all required items or not                                                 |
|                              |                    |                                                                                                    |
| **LootChestObjective**       | lc                 | Name of the loot chest needs to be opened                                                          |
|                              | lcopened           | Lootchest opened or not                                                                            |
|                              |                    |                                                                                                    |
| **MobObjective**             | mobkill            | Mob that has to be killed                                                                          |
|                              | mobkilled          | Mob dead or not                                                                                    |
|                              | mobamtkill         | Mob that requires certain amount of kills                                                          |
|                              | mobamtmax          | Amount of mob that players need to kill                                                            |
|                              | mobamtkilled       | Amount of mob killed                                                                               |
|                              |                    |                                                                                                    |
| **MythicMobObjective**       | mobkill            | Mob that has to be killed                                                                          |
|                              | mobkilled          | Mob dead or not                                                                                    |
|                              | mobamtkill         | Mob that requires certain amount of kills                                                          |
|                              | mobamtmax          | Amount of mob that players need to kill                                                            |
|                              | mobamtkilled       | Amount of mob killed                                                                               |
|                              | mobminlevel        | Minimum level of mob that players need to kill                                                     |
|                              | mobmaxlevel        | Maximum level of mob that players need to kill                                                     |
|                              |                    |                                                                                                    |
| **NPCInteractObjective**     | npcname            | Name of the NPC                                                                                    |
|                              | npcinteract        | Left click, Right click or both accepted                                                           |
|                              | npcinteracted      | Did the player interact with NPC or not                                                            |
|                              |                    |                                                                                                    |
| **PlaceholderObjective**     | scoreboard         | Alternative text shown on scoreboard                                                               |
|                              |                    |                                                                                                    |
| **PlayerPickupObjective**    | item               | Item required player to pick up                                                                    |
|                              | picked             | Is the item picked up or not                                                                       |
|                              |                    |                                                                                                    |
| **RedstonePowerObjective**   | min                | Minimum redstone power required                                                                    |
|                              | max                | Maximum redstone power required                                                                    |
|                              |                    |                                                                                                    |
| **TimerObjective**           | time               | Time required                                                                                      |
|                              | scoreboard         | Alternative text shown on scoreboard                                                               |
