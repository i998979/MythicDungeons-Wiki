# Dungeon

## Dungeon Commands & Permissions

Dungeon command: `/mythicdungeons, /mdungeons, /mdungeon, /md`

{% hint style="info" %}
Arguments inside `<>` are required and arguments inside `[]` are optional.
{% endhint %}

| Commands                                                                                                   | Permissions                                                            | Usage                                                                           |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| /MythicDungeons                                                                                            | MythicDungeons.Commands.Dungeons                                       | Show the help page                                                              |
| /MythicDungeons Reload \[Group \| Player \| LootTable \| Scoreboard \| Effect \| Locale \| Config \| Menu] | MythicDungeons.Commands.Dungeons.Reload                                | Reload specified dungeon configurations, leave it blank to reload all           |
| /MythicDungeons Chat \<Message> (or /dungeonchat /dchat /dc)                                               | MythicDungeons.Commands.Dungeons.Chat                                  | Chat with the dungeon members                                                   |
|                                                                                                            | MythicDungeons.Commands.Dungeons.Chat.ColorCode.\[0-9,a-f,k,l,m,n,o,r] | Use specific kind of color code in Dungeon Chat                                 |
| /MythicDungeons Create \<Type>                                                                             | MythicDungeons.Commands.Dungeons.Create                                | Create a new dungeon with specified dungeon group                               |
| /MythicDungeons Info \<Type> \[Id]                                                                         | MythicDungeons.Commands.Dungeons.Info                                  | Show specified dungeon's info. Enter id for more information                    |
| /MythicDungeons Join \<Type> \[Id]                                                                         | MythicDungeons.Commands.Dungeons.Join                                  | Join first available dungeon if id not specified. Otherwise, join specified one |
| /MythicDungeons Leave                                                                                      | MythicDungeons.Commands.Dungeons.Leave                                 | Leave the dungeon currently at                                                  |
| /MythicDungeons Remove \<Type> \<Id> \<Player>                                                             | MythicDungeons.Commands.Dungeons.Remove                                | Remove specified player from specified dungeon                                  |
| /MythicDungeons Start \<Type> \<Id>                                                                        | MythicDungeons.Commands.Dungeons.Start                                 | Start specified dungeon                                                         |
| /MythicDungeons Stop \<Type> \<Id>                                                                         | MythicDungeons.Commands.Dungeons.Stop                                  | Stop specified dungeon                                                          |
