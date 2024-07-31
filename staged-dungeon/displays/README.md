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

| Objective                | Placeholder        | Explanation |
| ------------------------ | ------------------ | ----------- |
| BlockBreakObjective      | broke              |             |
|                          | amount             |             |
|                          | block              |             |
|                          | world1, x1, y1, z1 |             |
|                          | world2, x2, y2, z2 |             |
|                          | progress           |             |
| BlockPlaceObjective      | placed             |             |
|                          | amount             |             |
|                          | block              |             |
|                          | world1, x1, y1, z1 |             |
|                          | world2, x2, y2, z2 |             |
|                          | progress           |             |
| BlockInteractObjective   | placed             |             |
|                          | amount             |             |
|                          | block              |             |
|                          | world1, x1, y1, z1 |             |
|                          | world2, x2, y2, z2 |             |
|                          | progress           |             |
| BuffClaimObjective       | bf                 |             |
|                          | bfclaimed          |             |
|                          | progress           |             |
| ChatMessageObjective     | chatscoreboard     |             |
|                          | chathassaid        |             |
|                          | progress           |             |
| CheckpointObjective      | cp                 |             |
|                          | cpreached          |             |
|                          | progress           |             |
| ContainerPickupObjective | world, x, y, z     |             |
|                          | item               |             |
|                          | amount             |             |
|                          | picked             |             |
|                          | progress           |             |
| DamageObjective          | damage             |             |
|                          | time               |             |
|                          | damaged            |             |
|                          | progress           |             |
| HasItemObjective         | item               |             |
|                          | amount             |             |
|                          | hasitem            |             |
|                          | progress           |             |
| LootChestObjective       | lc                 |             |
|                          | lcopened           |             |
|                          | progress           |             |
| MobObjective             | mobkill            |             |
|                          | mobkilled          |             |
|                          | progress           |             |
|                          | mobamtkill         |             |
|                          | mobamtmax          |             |
|                          | mobamtkilled       |             |
|                          | progress           |             |
| MythicMobObjective       | mobkill            |             |
|                          | mobkilled          |             |
|                          | progress           |             |
|                          | mobamtkill         |             |
|                          | mobamtmax          |             |
|                          | mobamtkilled       |             |
|                          | progress           |             |
|                          | mobminlevel        |             |
|                          | mobmaxlevel        |             |
| NPCInteractObjective     | npcname            |             |
|                          | npcinteracted      |             |
|                          | npcinteract        |             |
|                          | progress           |             |
| PlaceholderObjective     | scoreboard         |             |
| PlayerPickupObjective    | item               |             |
|                          | picked             |             |
|                          | progress           |             |
| RedstonePowerObjective   | min                |             |
|                          | max                |             |
|                          | progress           |             |
| TimerObjective           | time               |             |
|                          | scoreboard         |             |
|                          | progress           |             |
