# Action List

## Under `Ruins.Stages.<ID>.Actions`,  `Ruins.Stages.<ID>.Completions` & `Ruins.Stages.<ID>.FailActions`:

{% hint style="info" %}
**Reminder:** If the parameters are located under `Actions`, the list of actions will be done when the stage starts.

If the parameters are located under `Completions`, the list of actions will be done after all objectives of this stage are completed.
{% endhint %}

### Buff

| Parameters | Explanation                                                                                                            | Examples                                                     | Required |
| ---------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ | -------- |
| **Buff**   | Change declared buff's attributes                                                                                      | `Buff{id="1";enabled=false}`                                 |          |
| id         | ID of the declared buff                                                                                                |                                                              |          |
| enabled    | Whether this buff is enabled or not                                                                                    | `true` or `false`                                            |          |
| type       | Type of the buff                                                                                                       | `ONETIME` or `REPEAT`                                        |          |
| renew      | How long in ticks will the buff claimable again                                                                        |                                                              |          |
| perplayer  | If `true`, when the player claimed the buff, othters can still claim the buff. Otherwise, others cannot claim the buff | `true` or `false`                                            |          |
| toteam     | Is the buff effects apply to team                                                                                      | `true` or `false`                                            |          |
| refresh    | Make the buff claimable again instantly                                                                                | `true`                                                       |          |
| \<index>   | Potion effects to apply                                                                                                | `0='SPEED 10 2 true true true';1='JUMP 10 2 true true true'` |          |

### CancelStage

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>CancelStage</strong></td><td>Cancel specified stage</td><td><code>CancelStage{stage='1'}</code></td><td></td></tr><tr><td>stage</td><td>Stage to cancel</td><td></td><td>true</td></tr></tbody></table>

### Checkpoint

| Parameters     | Explanation                                                         | Examples                           | Required |
| -------------- | ------------------------------------------------------------------- | ---------------------------------- | -------- |
| **Checkpoint** | Change declared checkpoint's attributes                             | `Checkpoint{id="1";enabled=false}` |          |
| id             | ID of the declared checkpoint                                       |                                    |          |
| enabled        | Whether this checkpoint is enabled or not                           | `true` or `false`                  |          |
| reached        | Change the reached state of the checkpoint so that it can be reused | `true` or `false`                  |          |

### Command

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Command</strong></td><td>Send command from the server console</td><td><code>Command{from=CONSOLE;command='give %player% GOLDEN_CARROT 1'}</code></td><td></td></tr><tr><td><del>once</del></td><td><del>How the command executes</del></td><td><del><code>true</code> if the command only executes once, otherwise, the command will execute depending on how many players are online in the dungeon</del></td><td></td></tr><tr><td>from</td><td>Who will execute the command</td><td><code>CONSOLE</code> if the command is sent from the server, if it is not set, the command will be sent from the player</td><td></td></tr><tr><td>chance</td><td>Chance of this command will be executed</td><td><code>0.0</code> if the command never runs, <code>1.0</code> if the command runs every time</td><td></td></tr><tr><td>command</td><td>Command to send from the server console, use <code>%player%</code> to replace the player's name</td><td><code>give %player% GOLDEN_CARROT 1</code></td><td>true</td></tr></tbody></table>

### **Effect (EffectLib)**

| Parameters     | Explanation                                            | Examples                                                              | Required                         |
| -------------- | ------------------------------------------------------ | --------------------------------------------------------------------- | -------------------------------- |
| **Effect**     | Spawn EffectLib particles                              | `Effect{id=effectA;type=vortex;world=dungeon;x=120.5;y=5.0;z=259.5;}` |                                  |
| id             | ID of the effect if you want to remove it later        |                                                                       | `true` if `remove` is configured |
| remove         | Remove the particles so that it does not spawn anymore | `true` of the effect is being removed                                 |                                  |
| type           | Type of the effect declared in `effects.yml`           |                                                                       | true                             |
| world, x, y, z | Location to spawn the particles                        |                                                                       | true                             |

### Fly

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Fly</strong></td><td>Toggle player flight state</td><td><code>Fly{enabled=true}</code></td><td></td></tr><tr><td>enabled</td><td>Enable or disable player's flight state</td><td><code>true</code> or <code>false</code></td><td>true</td></tr></tbody></table>

### GameMode

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>GameMode</strong></td><td>Change player's gamemode</td><td><code>GameMode{mode=SURVIVAL}</code></td><td></td></tr><tr><td>gamemode</td><td>Change the player's gamemode, it follows the rule from <a href="https://hub.spigotmc.org/javadocs/spigot/org/bukkit/GameMode.html">Spigot API</a></td><td><code>SURVIVAL</code></td><td>true</td></tr></tbody></table>

### Hologram (Hologram Plugin)

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Hologram</strong></td><td>Create hologram in specified location</td><td><code>Hologram{id=0;world=dungeon;x=120.5;y=9.0;z=259.5;0="Line 0";1="{material=PLAYER_HEAD;glow=true;damage=0;custommodeldata=1;skullowner=991d961c-b6b4-4d49-88e6-01788cf445dc}"}</code></td><td></td></tr><tr><td>id</td><td>ID of the hologram</td><td> </td><td>true</td></tr><tr><td>hide</td><td>Hide/show the hologram</td><td><code>true</code> or <code>false</code></td><td></td></tr><tr><td>remove</td><td>Remove the hologram, cannot be modified or shown again</td><td><code>true</code></td><td></td></tr><tr><td>world, x, y, z</td><td>Location of the hologram, changing the location moves the hologram</td><td></td><td>true if firstly created</td></tr><tr><td>&#x3C;line></td><td>Set/modify lines of the hologram, loaded 1 by 1, empty line still occupies a line.</td><td></td><td>true if firstly created</td></tr></tbody></table>

### Item

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Item</strong></td><td>Drop specified item on ground</td><td><code>Item{item='{"v":3105,"type":"REDSTONE_BLOCK"}';world=dungeon;x=116.0;y=5.0;z=255.0}</code></td><td></td></tr><tr><td>item</td><td>Item to drop, type <code>/mg check</code> to get the formatted string</td><td><code>{"v":3105,"type":"REDSTONE_BLOCK"}</code></td><td>true</td></tr><tr><td>world, x, y, z, yaw, pitch</td><td>Location to drop the item</td><td></td><td>true</td></tr></tbody></table>

### LootChest

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>LootChest</strong></td><td>Change declared loot chest's attributes</td><td><code>LootChest{id=0;enabled=true;type=CHEST;perplayer=true;renew=60;0='{"v":2865,"type":"REDSTONE_BLOCK"}';53='MythicMobs{id="SkeletonKingSword";amount=2}'}</code></td><td></td></tr><tr><td>id</td><td>ID of the loot chest that its behaviour needs to be changed</td><td></td><td></td></tr><tr><td>enabled</td><td>Whether this loot chest is enabled or not. If it is not enabled, the loot chest has no effect when opened</td><td><code>true</code> or <code>false</code></td><td></td></tr><tr><td>type</td><td>Inventory type of the loot chest, It follows the rule from <a href="https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/inventory/InventoryType.html">Spigot API</a></td><td><code>CHEST</code> if the inventory type is a chest</td><td></td></tr><tr><td>perplayer</td><td>Is the loot chest content unique for all players or they all share the same loot chest content</td><td><code>true</code> or <code>false</code></td><td></td></tr><tr><td>renew</td><td>How long in ticks will the loot chest content renew, only applicable if <code>perplayer</code> is <code>true</code></td><td>Enter number that is larger than dungeon timer for no renew</td><td></td></tr><tr><td>title</td><td>Title of the loot chest inventory</td><td></td><td></td></tr><tr><td>size</td><td>Size of the loot chest inventory, only applicable if <code>type</code> is <code>CHEST</code></td><td></td><td></td></tr><tr><td>&#x3C;slot></td><td>Item in the specified slot, type <code>/mg check</code> to get the formatted string</td><td><code>0='{"v":2865,"type":"REDSTONE_BLOCK"}'</code> means changing slot <code>0</code> into <code>REDSTONE_BLOCK</code>, <code>0='null'</code> means removing item in slot <code>0</code>}</td><td></td></tr></tbody></table>

### Look (Citizens)

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Look</strong></td><td>Make Citizens NPC declared in <code>MythicDungeons/groups/&#x3C;Dungeon Type>/npcs.yml</code> look at location</td><td><code>Look{id=1;world=dungeon;x=116.0;y=5.0;z=255.0;pitch=0.0;yaw=0.0}</code></td><td></td></tr><tr><td>id</td><td>ID of the NPC declared in <code>MythicDungeons/groups/&#x3C;Dungeon Type>/npcs.yml</code></td><td></td><td>true</td></tr><tr><td>world, x, y, z, yaw, pitch</td><td>Location the NPC will look at</td><td></td><td>true</td></tr></tbody></table>

### Message

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Message</strong></td><td>Send a message to everyone in the dungeon instance</td><td><code>Message{type=ACTION_BAR;text='&#x26;c&#x26;lGOOD, continue your journey, legends.'}</code></td><td></td></tr><tr><td>type</td><td>Message type</td><td><code>CHAT</code> if it is sent to chat, <code>ACTION_BAR</code> if it is sent to action bar, <code>TITLE</code> if it is sent to title</td><td>true if <code>clear</code> is not set</td></tr><tr><td>text</td><td>Message to send, use <code>%player%</code> to replace the player's name</td><td></td><td>true if <code>type</code> is <code>CHAT</code> or <code>ACTION_BAR</code></td></tr><tr><td>clear</td><td>Clear the current showing title</td><td><code>true</code> if the title is being cleared</td><td></td></tr><tr><td>title</td><td>Title of the title message</td><td></td><td></td></tr><tr><td>subtitle</td><td>Subtitle of the title message</td><td></td><td></td></tr><tr><td>fadein</td><td>How long in ticks of fade in time of title message</td><td></td><td></td></tr><tr><td>stay</td><td>How long in ticks of stay time of title message</td><td></td><td></td></tr><tr><td>fadeout</td><td>How long in ticks of fade out time of title message</td><td></td><td></td></tr></tbody></table>

### PathTo (Citizens)

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>PathTo</strong></td><td>Make Citizens NPC declared in <code>MythicDungeons/groups/&#x3C;Dungeon Type>/npcs.yml</code> pathfind to location</td><td><code>PathTo{id=1;world=dungeon;x=116.0;y=5.0;z=255.0;pitch=0.0;yaw=0.0}</code></td><td></td></tr><tr><td>id</td><td>ID of the NPC declared in <code>MythicDungeons/groups/&#x3C;Dungeon Type>/npcs.yml</code></td><td></td><td>true</td></tr><tr><td>world, x, y, z, yaw, pitch</td><td>Location the NPC will pathfind to</td><td></td><td>true</td></tr></tbody></table>

### Sound

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Sound</strong></td><td>Play specified sound at location</td><td><code>Sound{world=dungeon;x=116.0;y=5.0;z=255.0;category=MASTER;sound=block.anvil.use;volume=1;pitch=1}</code></td><td></td></tr><tr><td>stop</td><td>Stop playing sound specified by <code>sound</code></td><td><code>true</code> if the playing sound is being stopped</td><td></td></tr><tr><td>sound</td><td>Sound to play or stop</td><td></td><td>true</td></tr><tr><td>category</td><td>Category of the sound</td><td></td><td>true if <code>stop</code> is not set</td></tr><tr><td>sound</td><td>Volume of the sound</td><td></td><td>true if <code>stop</code> is not set</td></tr><tr><td>pitch</td><td>Pitch of the sound</td><td></td><td>true if <code>stop</code> is not set</td></tr><tr><td>world, x, y, z</td><td>Origin of the sound</td><td></td><td>true if <code>stop</code> is not set</td></tr></tbody></table>

### Spawn (Citizens)

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Spawn</strong></td><td>Spawn Citizens NPC declared in <code>MythicDungeons/groups/&#x3C;Dungeon Type>/npcs.yml</code> into world</td><td><code>Spawn{id=1;world=dungeon;x=116.0;y=5.0;z=255.0;pitch=0.0;yaw=0.0}</code></td><td></td></tr><tr><td>id</td><td>ID of the NPC declared in <code>MythicDungeons/groups/&#x3C;Dungeon Type>/npcs.yml</code></td><td></td><td>true</td></tr><tr><td>world, x, y, z, yaw, pitch</td><td>Location of the NPC to spawn</td><td></td><td>true</td></tr></tbody></table>

### TakeItem

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>TakeItem</strong></td><td>Take item from player's inventory</td><td><code>TakeItem{allPlayer=true;0='{"v":3105,"type":"REDSTONE_BLOCK"}'}</code></td><td></td></tr><tr><td>allplayer</td><td>Take specified items from all players or not</td><td><code>true</code> if items are taken from all dungeon players</td><td></td></tr><tr><td>&#x3C;id></td><td>ID is meaningless, but it must be an integer. What item will take, type <code>/mg check</code> to get the formatted string</td><td><code>0='{"v":3105,"type":"REDSTONE_BLOCK"}'</code></td><td>true</td></tr></tbody></table>

### TeleportTo (Citizens)

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>TeleportTo</strong></td><td>Teleport Citizens NPC declared in <code>MythicDungeons/groups/&#x3C;Dungeon Type>/npcs.yml</code> into location</td><td><code>TeleportTo{id=1;world=dungeon;x=116.0;y=5.0;z=255.0;pitch=0.0;yaw=0.0}</code></td><td></td></tr><tr><td>id</td><td>ID of the NPC declared in <code>MythicDungeons/groups/&#x3C;Dungeon Type>/npcs.yml</code></td><td></td><td>true</td></tr><tr><td>world, x, y, z, yaw, pitch</td><td>Location to teleport the NPC</td><td></td><td>true</td></tr></tbody></table>

### Teleport

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Teleport</strong></td><td>Teleport player to specified location</td><td><code>Teleport{world=dungeon;x=116.0;y=5.0;z=255.0;pitch=0.0;yaw=0.0;radius=5}</code></td><td></td></tr><tr><td>world, x, y, z, yaw, pitch</td><td>Location to teleport</td><td></td><td>true</td></tr><tr><td>radius</td><td>Random horizontal offset of the teleport location</td><td></td><td></td></tr></tbody></table>

### Teleporter

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th width="167">Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Teleporter</strong></td><td>Change declared teleporter's attributes</td><td><code>Teleporter{id="1";enabled=false}</code></td><td></td></tr><tr><td>id</td><td>ID of the declared teleporter</td><td></td><td>true</td></tr><tr><td>enabled</td><td>Whether this teleporter is enabled or not</td><td><code>true</code> or <code>false</code></td><td></td></tr><tr><td>cooldown</td><td>Cooldown in ticks of the teleporter</td><td></td><td></td></tr><tr><td>world, x, y, z, yaw, pitch</td><td>Destination of the teleporter</td><td></td><td></td></tr></tbody></table>

### Trap

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th width="167">Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>Trap</strong></td><td>Change declared trap's attributes</td><td><code>Trap{id="1";enabled=false}</code></td><td></td></tr><tr><td>id</td><td>ID of the declared trap</td><td></td><td>true</td></tr><tr><td>enabled</td><td>Whether this trap is enabled or not</td><td><code>true</code> or <code>false</code></td><td></td></tr><tr><td>interval</td><td>Interval in ticks per trap action</td><td></td><td>Only applicable to Damage Trap and Arrow Trap</td></tr><tr><td>damage</td><td>Damage of the trap</td><td></td><td></td></tr><tr><td>fireticks</td><td>How long in ticks will the player be set on fire</td><td></td><td>Only applicable to Arrow Trap and Fire Trap</td></tr><tr><td>velocity</td><td>How fast will the arrow fly</td><td></td><td>Only applicable to Arrow Trap</td></tr><tr><td>count</td><td>On/Off interval of fire trap</td><td><code>10 10 20 10 40 10</code> means the particle spawns for 10, 20, 40 ticks and 10 ticks between them</td><td>Only applicable to Fire Trap</td></tr></tbody></table>

### MythicMob

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>MythicMob</strong></td><td>Spawn a MythicMobs mob</td><td><code>MythicMob{type=rat3;at=LOCATION;world=dungeon;x=120.5;y=5.0;z=259.5;yaw=180.0;pitch=0.0}</code> or <code>MythicMob{type=rat4;at=NEARBY;radius=10.0}</code></td><td></td></tr><tr><td>type</td><td>Type of the MythicMob defined in <code>MythicMobs/Mobs/&#x3C;Yml containing the mob>.yml</code></td><td></td><td>true</td></tr><tr><td>at</td><td>Where will the mob spawn</td><td><code>LOCATION</code> if the mob spawns in a specified location, <code>NEARBY</code> if the mob spawns in a radius of the player</td><td>true</td></tr><tr><td>world, x, y, z, yaw, pitch</td><td>Location to spawn the mob</td><td></td><td>true if <code>at</code> is <code>LOCATION</code></td></tr><tr><td>radius</td><td>Radius of the mob will spawn near the player</td><td></td><td>true if <code>at</code> is <code>NEARBY</code></td></tr><tr><td>minlevel</td><td>Minimum level of the mob will spawn</td><td></td><td></td></tr><tr><td>maxlevel</td><td>Maximum level of the mob will spawn</td><td></td><td></td></tr></tbody></table>

### MythicSpawner

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>MythicSpawner</strong></td><td>Create a MythicMobs spawner</td><td><code>MythicSpawner{id=SpawnerA;type=rat1;world=dungeon;x=116.0;y=5.0;z=255.0;yaw=0.0;pitch=0.0;settings=rat1.yml}</code></td><td></td></tr><tr><td>id</td><td>ID of the spawner</td><td></td><td>true if <code>enabled</code> or <code>remove</code> is configured</td></tr><tr><td>enabled</td><td>Is this spawner enabled, if it is not enabled, the spawner will not spawn mobs. The spawner is enabled by default when it is first declared</td><td><code>true</code> or <code>false</code></td><td></td></tr><tr><td>remove</td><td>Whether this spawner is being removed or not. Once it is removed, it can not be enabled</td><td><code>true</code> if the spawner is being removed</td><td></td></tr><tr><td>type</td><td>Type of the MythicMob defined in <code>MythicMobs/Mobs/&#x3C;Yml containing the mob>.yml</code>, multiple mobs with different weightings can be defined by following the rule <a href="https://git.mythiccraft.io/mythiccraft/MythicMobs/-/wikis/Spawners">here</a></td><td></td><td>true</td></tr><tr><td>world, x, y, z, yaw, pitch</td><td>Location of the spawner</td><td></td><td>true</td></tr><tr><td>settings</td><td>Settings of the spawner located at <code>MythicDungeons/groups/&#x3C;Dungeon Type>/spawners</code>, it configures the behaviour of the spawner created, follows the rule from <a href="https://git.mythiccraft.io/mythiccraft/MythicMobs/-/wikis/Spawners">here</a>. However, <code>X, Y, Z</code> is overridden by the plugin and it can be left blank, and <code>MobName</code> is also overridden by the plugin since it cannot be blank, so a valid mob name is required</td><td></td><td></td></tr></tbody></table>

### PasteSchematic

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th><th>Required</th></tr></thead><tbody><tr><td><strong>PasteSchematic</strong></td><td>Paste schematic in specified location</td><td><code>PasteSchematic{file=bridge;world=dungeon;x=116.0;y=5.0;z=255.0;pitch=0.0;yaw=0.0}</code></td><td></td></tr><tr><td>file</td><td>Schematic file stored in <code>MythicDungeons/groups/&#x3C;Dungeon Type>/schematics</code></td><td></td><td>true</td></tr><tr><td>world, x, y, z</td><td>Location to paste the schematic</td><td></td><td></td></tr></tbody></table>
