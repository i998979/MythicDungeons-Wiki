# Scoreboard

Scoreboard Display makes use of the scoreboard to display dungeon information like the time before dungeon expires, the dungeon currently challenging, and objectives of the current stage.

Unlike `BossBar` and `ActionBar`, if the options (except `Objectives`) are defined,  once that stage is active, it will be inherited until the next stage with those options defined.

## Under `Stages.<ID>.Displays.Scoreboard`:

| Option         | Explanation                                              |
| -------------- | -------------------------------------------------------- |
| Interval       | Interval before showing the next title line              |
| Title          | Titles to display                                        |
| ScrollInterval | Scroll interval before showing the next information line |
| Lines          | Information lines to display                             |
| Objectives     | Objectives to display                                    |
