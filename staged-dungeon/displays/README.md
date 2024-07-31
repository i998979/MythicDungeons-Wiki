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

Placeholders are used within Displays to display objective-specific information. It can be used like `%<objective type>_<objective order>_<placeholder>%`. For example, `%MythicMobs_1_mobamtkill%` shows the mob's name required to kill in [MythicMobs Objective](../actions-completions-and-fail-actions/action-list.md#mythicmob-mythicmobs).

## General Placeholders

| Placeholder | Explanation                                   |
| ----------- | --------------------------------------------- |
| progress    | Progress of the objective between 0.0 and 1.0 |

## Placeholders

| Objective           | Placeholder        | Explanation                                                                                        |
| ------------------- | ------------------ | -------------------------------------------------------------------------------------------------- |
| **BlockBreak**      | broke              | Blocks broke                                                                                       |
|                     | amount             | Amount of blocks needed to break                                                                   |
|                     | block              | Block type required to break                                                                       |
|                     | world1, x1, y1, z1 | First corner of the region                                                                         |
|                     | world2, x2, y2, z2 | Second corner of the region                                                                        |
|                     |                    |                                                                                                    |
| **BlockPlace**      | placed             | Blocks placed                                                                                      |
|                     | amount             | Amount of blocks needed to place                                                                   |
|                     | block              | Block type required to place                                                                       |
|                     | world1, x1, y1, z1 | First corner of the region                                                                         |
|                     | world2, x2, y2, z2 | Second corner of the region                                                                        |
|                     |                    |                                                                                                    |
| **BlockInteract**   | placed             | Block interacted                                                                                   |
|                     | amount             | Amount of blocks needed to interact                                                                |
|                     | block              | Block type required to interact                                                                    |
|                     | world1, x1, y1, z1 | First corner of the region                                                                         |
|                     | world2, x2, y2, z2 | Second corner of the region                                                                        |
|                     |                    |                                                                                                    |
| **BuffClaim**       | bf                 | Buff required to claim                                                                             |
|                     | bfclaimed          | Is this buff claimed                                                                               |
|                     |                    |                                                                                                    |
| **ChatMessage**     | chatscoreboard     | Chat message required, scoreboard text is additionally defined in action                           |
|                     | chathassaid        | Is this message has been said by players                                                           |
|                     |                    |                                                                                                    |
| **Checkpoint**      | cp                 | Name of the checkpoint needs to be reached                                                         |
|                     | cpreached          | Checkpoint reached or not                                                                          |
|                     |                    |                                                                                                    |
| **ContainerPickup** | world, x, y, z     | Location of the container                                                                          |
|                     | item               | Item to sacrifice                                                                                  |
|                     | amount             | Amount to sacrifice                                                                                |
|                     | picked             | Is the item picked up by container                                                                 |
|                     |                    |                                                                                                    |
| **Damage**          | damage             | Damage to take                                                                                     |
|                     | time               | Times of the damage to take                                                                        |
|                     | damaged            | Times of the damage taken                                                                          |
|                     |                    |                                                                                                    |
| **HasItem**         | item               | Display name of the item required, if the item has no display name, material name is shown instead |
|                     | amount             | Amount of the item required                                                                        |
|                     | hasitem            | Does any/all player have all required items or not                                                 |
|                     |                    |                                                                                                    |
| **LootChest**       | lc                 | Name of the loot chest needs to be opened                                                          |
|                     | lcopened           | Lootchest opened or not                                                                            |
|                     |                    |                                                                                                    |
| **Mob**             | mobkill            | Mob that has to be killed                                                                          |
|                     | mobkilled          | Mob dead or not                                                                                    |
|                     | mobamtkill         | Mob that requires certain amount of kills                                                          |
|                     | mobamtmax          | Amount of mob that players need to kill                                                            |
|                     | mobamtkilled       | Amount of mob killed                                                                               |
|                     |                    |                                                                                                    |
| **MythicMob**       | mobkill            | Mob that has to be killed                                                                          |
|                     | mobkilled          | Mob dead or not                                                                                    |
|                     | mobamtkill         | Mob that requires certain amount of kills                                                          |
|                     | mobamtmax          | Amount of mob that players need to kill                                                            |
|                     | mobamtkilled       | Amount of mob killed                                                                               |
|                     | mobminlevel        | Minimum level of mob that players need to kill                                                     |
|                     | mobmaxlevel        | Maximum level of mob that players need to kill                                                     |
|                     |                    |                                                                                                    |
| **NPCInteract**     | npcname            | Name of the NPC                                                                                    |
|                     | npcinteract        | Left click, Right click or both accepted                                                           |
|                     | npcinteracted      | Did the player interact with NPC or not                                                            |
|                     |                    |                                                                                                    |
| **Placeholder**     | scoreboard         | Alternative text shown on scoreboard                                                               |
|                     |                    |                                                                                                    |
| **PlayerPickup**    | item               | Item required player to pick up                                                                    |
|                     | picked             | Is the item picked up or not                                                                       |
|                     |                    |                                                                                                    |
| **RedstonePower**   | min                | Minimum redstone power required                                                                    |
|                     | max                | Maximum redstone power required                                                                    |
|                     |                    |                                                                                                    |
| **Timer**           | time               | Time required                                                                                      |
|                     | scoreboard         | Alternative text shown on scoreboard                                                               |
