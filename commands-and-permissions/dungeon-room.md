# Dungeon Room

## Dungeon Room Commands & Permissions

Dungeon Room command: `/mythicrooms, /mrm, /room, /mr`

{% hint style="info" %}
Arguments inside `<>` are required and arguments inside `[]` are optional.
{% endhint %}

| Commands                                                        | Permissions                                                         | Usage                                                                                         |
| --------------------------------------------------------------- | ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| /MythicRooms                                                    | MythicDungeons.Commands.Rooms                                       | Show the help page                                                                            |
| /MythicRooms Accept \<Player>                                   | MythicDungeons.Commands.Rooms.Invite.Accept                         | Accept specified player's invitation                                                          |
| /MythicRooms AllInvite                                          | MythicDungeons.Commands.Rooms.AllInvite                             | Give/revoke permission that all members can invite other players                              |
| /MythicRooms Chat \<Message> (or /roomchat, /rmchat, /rc)       | MythicDungeons.Commands.Rooms.Chat                                  | Chat with the members                                                                         |
|                                                                 | MythicDungeons.Commands.Rooms.Chat.ColorCode.\[0-9,a-f,k,l,m,n,o,r] | Use specific kind of color code in Room Chat                                                  |
| /MythicRooms Create \<Type>                                     | MythicDungeons.Commands.Rooms.Create                                | Create a room with a specified dungeon type                                                   |
| /MythicRooms Deny \<Player>                                     | MythicDungeons.Commands.Rooms.Invite.Deny                           | Decline specified player's invitation                                                         |
| /MythicRooms Disband                                            | MythicDungeons.Commands.Rooms.Disband                               | Disband the room. All members will be removed                                                 |
| /MythicRooms Info                                               | MythicDungeons.Commands.Rooms.Info                                  | Shows the room info.                                                                          |
| /MythicRooms Invite \<Player>                                   | MythicDungeons.Commands.Rooms.Invite                                | Invite a specified player to the room                                                         |
| /MythicRooms Join \<Id / Player>                                | MythicDungeons.Commands.Rooms.Join                                  | Join the room with specified id/owner                                                         |
| /MythicRooms Leave                                              | MythicDungeons.Commands.Rooms.Leave                                 | Leave the room                                                                                |
| /MythicRooms MaxPlayer \<Amount>                                | MythicDungeons.Commands.Rooms.MaxPlayer                             | Change how many players the room accepts                                                      |
| /MythicRooms Menu \[Menu/Room]                                  | MythicDungeons.Commands.Rooms.Menu                                  | Open specified menu. Leave it blank to open Main Menu                                         |
| /MythicRooms Note \[Note]                                       | MythicDungeons.Commands.Rooms.Note                                  | Change room's note. Leave it blank to clear                                                   |
| MythicRooms MinPlayer \<Amount>                                 | MythicDungeons.Commands.Rooms.MinPlayer                             | Change how many players the room requires                                                     |
| /MythicRooms Privacy \<PUBLIC / PRIVATE / PASSWORD> \[Password] | MythicDungeons.Commands.Rooms.Privacy                               | Change room's privacy settings. Please enter the password if privacy has been set to PASSWORD |
| /MythicRooms Promote \<Player>                                  | MythicDungeons.Commands.Rooms.Promote                               | Promote specified players. You will lose all permission after promoting others                |
| /MythicRooms Queue \<Type>                                      | MythicDungeons.Commands.Rooms.Queue                                 | Join or create a queue with a specified dungeon type                                          |
| /MythicRooms Remove \<Player>                                   | MythicDungeons.Commands.Rooms.Remove                                | Remove specified player from the room                                                         |
| /MythicRooms Start                                              | MythicDungeons.Commands.Rooms.Start                                 | Start challenging the dungeon                                                                 |
