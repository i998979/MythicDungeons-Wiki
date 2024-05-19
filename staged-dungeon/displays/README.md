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

## Placeholders

Placeholders are used within Displays to display objective-specific information. It can be used like `%<objective type>_<objective order>_<placeholder>%`. For example, `%MythicMobs_1_mobamtkill%` shows the name of the mob required to kill in [MythicMobs Objective](../objectives/objective-list.md#mythicmob).

| Objectives | Placeholders | Explanation |
| ---------- | ------------ | ----------- |
|            |              |             |
|            |              |             |
|            |              |             |
