# Ways To Join Dungeon

## Commands

By typing `/mr create <type>`, a `Regular Room` with specified type will be created. You can either use command for other actions or use `/mr menu` to access the GUI for other actions. And `/mr queue <Type>`, it creates a temporary room and acts like a queue with a fixed size, like joining through Signs and NPCs. However, Dungeon Group type wanted to queue for has to be specified.

## GUIs

By typing `/mr menu`, a GUI will be opened, and you may search for `Regular Rooms` with specified dungeon type, invite other players to the room, and start challenging the dungeon.

## Signs

Joining dungeon through signs requires Join Sign location configured in the dungeon group config. Once you have it configured, when the player clicks the sign, they will be put into an existing `Temporary Room`, if there is no room at the moment, a new temporary room will be created and they will be put inside.

Also, you can configure a Leave Sign for players to leave the room.

## NPCs

Joining dungeon through NPCs requires [Citizens](https://www.spigotmc.org/resources/citizens.13811/) installed and NPC ID configured in the dungeon group config. It acts similarly to Signs.

You can also configure a Leave NPC for players to leave the room.
