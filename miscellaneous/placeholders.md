# Placeholders

Since 2.3.0-BETA, for the convenience of displaying different information in different ways, various PlaceholderAPI placeholders have been added.

Please make sure you have PlaceholderAPI installed properly.

{% hint style="warning" %}
**Warning:** Placeholder might not parse / return `...` or `none`if the player did not join any room / dungeon.

If your PlaceholderAPI's placeholder aren't parsing, please check [here](https://github.com/PlaceholderAPI/PlaceholderAPI/wiki/FAQ#it-only-shows-placeholder-and-not-the-variable).
{% endhint %}

## Dungeon Room Placeholders

| Placeholder                       | Explanation                         |
| --------------------------------- | ----------------------------------- |
| %mythicdungeons\_room\_type%      | Room's Dungeon Group                |
| %mythicdungeons\_room\_id%        | Room's ID                           |
| %mythicdungeons\_room\_current%   | Room's current players amount       |
| %mythicdungeons\_room\_minplayer% | Room's minimum players amount       |
| %mythicdungeons\_room\_maxplayer% | Room's maximum players amount       |
| %mythicdungeons\_room\_created%   | Timestamp of the room created       |
| %mythicdungeons\_room\_visible%   | Room's visibility in menu           |
| %mythicdungeons\_room\_owner%     | Room's owner (Regular Room only)    |
| %mythicdungeons\_room\_privacy%   | Room's privacy (Regular Room only)  |
| %mythicdungeons\_room\_password%  | Room's password (Regular Room only) |

## Dungeon Placeholders

|                                          |                                                                       |
| ---------------------------------------- | --------------------------------------------------------------------- |
| %mythicdungeons\_group\_name%            | Dungeon Group's name                                                  |
| %mythicdungeons\_group\_type%            | Dungeon Group's type                                                  |
| %mythicdungeons\_group\_minplayer%       | Dungeon Group's minimum players amount                                |
| %mythicdungeons\_group\_maxplayer%       | Dungeon Group's maximum players amount                                |
| %mythicdungeons\_group\_visible%         | Dungeon Group's visibility                                            |
| %mythicdungeons\_dungeon\_id%            | Dungeon's ID                                                          |
| %mythicdungeons\_dungeon\_origin\_world% | Dungeon's Origin world                                                |
| %mythicdungeons\_dungeon\_origin\_x%     | Dungeon's Origin x-axis                                               |
| %mythicdungeons\_dungeon\_origin\_y%     | Dungeon's Origin y-axis                                               |
| %mythicdungeons\_dungeon\_origin\_z%     | Dungeon's Origin z-axis                                               |
| %mythicdungeons\_dungeon\_current%       | Dungeon's current players amount                                      |
| %mythicdungeons\_dungeon\_playerdeath%   | Dungeon's player death count                                          |
| %mythicdungeons\_dungeon\_teamdeath%     | Dungeon's team death count                                            |
| %mythicdungeons\_dungeon\_startedat%     | Timestamp of the dungeon started                                      |
| %mythicdungeons\_dungeon\_state%         | Dungeon's state `(NOT_STARTED, PRE_STARTING, STARTED, ENDING, ENDED)` |
