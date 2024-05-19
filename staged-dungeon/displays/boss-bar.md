# Boss Bar

BossBar Display makes use of the boss bar to display dungeon information like the objectives of the current stage.

## Under `Stages.<ID>.Displays.BossBar`:

| Option   | Explanation                                 |
| -------- | ------------------------------------------- |
| Interval | Interval before showing the next title line |
| Lines    | Information lines to display                |

Additionally, other than plain text, there are multiple parameters can be defined in `Lines`.

| Parameter | Explanation                                                                                                                          | Example                                                                                                                         |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
|           |                                                                                                                                      | `{progress=1.0;color=PURPLE;style=SEGMENTED_20;message='&fDiscover the secret of %Checkpoint_2_cp%: %Checkpoint_2_cpreached%'}` |
| progress  | Progress of the boss bar, between 0.0 to 1.0, or make use of the placeholders                                                        | `1.0`, `%BlockBreak_3_progress%`                                                                                                |
| color     | Color of the boss bar, it follows the rule from [Spigot API](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/boss/BarColor.html) | `PURPLE`                                                                                                                        |
| style     | Style of the boss bar, it follows the rule from [Spigot API](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/boss/BarStyle.html) | `SEGMENTED_20`                                                                                                                  |
| message   | Message of the boss bar                                                                                                              |                                                                                                                                 |
