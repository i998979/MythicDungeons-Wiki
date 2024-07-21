# Objective List

## Under `Stages.<ID>.Objectives`:

### **BlockBreak**

<div align="left">

<figure><img src="../../.gitbook/assets/BlockBreakObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters         | Explanation                                                                                                                                                          | Examples                                                                                                                                      | Required                            |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| **BlockBreak**     | <p>Blocks in region required to break.<br><code>BlockBreak</code> option in <code>general.yml</code> still work, only matching blocks can be broken</p>              | `BlockBreak{world1=dungeon;x1=114;y1=4;z1=246;world2=dungeon;x2=126;y2=10;z2=264;material='STONE COBBLESTONE';type=AMOUNT_COMBINED;amount=3}` |                                     |
| world1, x1, y1, z1 | First corner of the region                                                                                                                                           |                                                                                                                                               | true                                |
| world2, x2, y2, z2 | Second corner of the region                                                                                                                                          |                                                                                                                                               | true                                |
| material           | Block material required to break, it follows the rule from [Spigot API](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html), multiple can be combined | `STONE COBBLESTONE`                                                                                                                           | true                                |
| type               | Checking type, whether all blocks in region are required to break or only certain amount                                                                             | `AMOUNT_COMBINED` or `ALL`                                                                                                                    |                                     |
| amount             | Amount of blocks required to break                                                                                                                                   |                                                                                                                                               | true if `type` is `AMOUNT_COMBINED` |

### BlockInteract

| Parameters         | Explanation                                                                                                                                                                         | Examples                                                                                                                                         | Required                            |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------- |
| **BlockInteract**  | <p>Blocks in region required to interact.<br><code>BlockInteract</code> option in <code>general.yml</code> still work, objective will still be triggered</p>                        | `BlockInteract{world1=dungeon;x1=114;y1=4;z1=246;world2=dungeon;x2=126;y2=10;z2=264;material='STONE COBBLESTONE';type=AMOUNT_COMBINED;amount=3}` |                                     |
| world1, x1, y1, z1 | First corner of the region                                                                                                                                                          |                                                                                                                                                  | true                                |
| world2, x2, y2, z2 | Second corner of the region                                                                                                                                                         |                                                                                                                                                  | true                                |
| left               | Is left-clicking accepted                                                                                                                                                           |                                                                                                                                                  | true                                |
| right              | Is right-clicking accepted                                                                                                                                                          |                                                                                                                                                  | true                                |
| cancel             | Is the action cancelled after interaction, levers will not be turned on, buttons will not output redstone signal                                                                    |                                                                                                                                                  | false                               |
| material           | Block material required to interact, it follows the rule from [Spigot API](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html), multiple can be combined with space  | `STONE COBBLESTONE`                                                                                                                              | true                                |
| type               | Checking type, whether all blocks in region are required to interact or only certain amount                                                                                         | `AMOUNT_COMBINED` or `ALL`                                                                                                                       |                                     |
| amount             | Amount of blocks required to interact                                                                                                                                               |                                                                                                                                                  | true if `type` is `AMOUNT_COMBINED` |

### BlockPlace

<div align="left">

<figure><img src="../../.gitbook/assets/BlockPlaceObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters         | Explanation                                                                                                                                                                      | Examples                                                                                                                                      | Required                            |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| **BlockPlace**     | <p>Blocks in region required to place.<br><code>BlockPlace</code> option in <code>general.yml</code> still work, only matching blocks can be placed</p>                          | `BlockPlace{world1=dungeon;x1=114;y1=4;z1=246;world2=dungeon;x2=126;y2=10;z2=264;material='STONE COBBLESTONE';type=AMOUNT_COMBINED;amount=3}` |                                     |
| world1, x1, y1, z1 | First corner of the region                                                                                                                                                       |                                                                                                                                               | true                                |
| world2, x2, y2, z2 | Second corner of the region                                                                                                                                                      |                                                                                                                                               | true                                |
| material           | Block material required to place, it follows the rule from [Spigot API](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html), multiple can be combined with space  | `STONE COBBLESTONE`                                                                                                                           | true                                |
| type               | Checking type, whether all blocks in region are required to place or only certain amount                                                                                         | `AMOUNT_COMBINED` or `ALL`                                                                                                                    |                                     |
| amount             | Amount of blocks required to place                                                                                                                                               |                                                                                                                                               | true if `type` is `AMOUNT_COMBINED` |

### BuffClaim

<div align="left">

<figure><img src="../../.gitbook/assets/BuffClaimObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters    | Explanation                                               | Examples          | Required |
| ------------- | --------------------------------------------------------- | ----------------- | -------- |
| **BuffClaim** | Buff required to claim                                    | `BuffClaim{id=1}` |          |
| id            | ID of the buff, it should be declared under `Ruins.Buffs` |                   | true     |

### **ChatMessage**

<div align="left">

<figure><img src="../../.gitbook/assets/ChatMessageObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters      | Explanation                                                                              | Examples                                                                             | Required |
| --------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ | -------- |
| **ChatMessage** | Message required to say in chat                                                          | `ChatMessage{message="hello world";scoreboard="greetings to the world";cancel=true}` |          |
| message         | Messages required to say, regular expressions are supported                              | `123[abc]456` for `123a456`, `123b456`, `123c456`                                    | true     |
| scoreboard      | Alternative text shown in scoreboard to avoid showing regular expressions directly on it |                                                                                      |          |
| cancel          | Is this message sent by the player not showing in chat                                   | `true` or `false`                                                                    |          |

### **Checkpoint**

<div align="left">

<figure><img src="../../.gitbook/assets/CheckpointObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters     | Explanation                                                       | Examples           | Required |
| -------------- | ----------------------------------------------------------------- | ------------------ | -------- |
| **Checkpoint** | Checkpoint required to capture                                    | `Checkpoint{id=1}` |          |
| id             | ID of the checkpoint, it should be declared in `checkpoints.yml`  |                    | true     |
| allplayer      | Are all players required to stay inside                           | `true` or `false`  |          |
| allpoint       | Are all points required to be captured at once                    | `true` or `false`  |          |
| time           | Time in ticks the player has to stay inside before it is captured |                    |          |
| sneak          | Is sneaking required to claim this checkpoint                     | `true` or `false`  |          |

### ContainerPickup

<div align="left">

<figure><img src="../../.gitbook/assets/ContainerPickupObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters          | Explanation                                                                                                                                                                | Examples                                                                                  | Required |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | -------- |
| **ContainerPickup** | Items required to throw into hopper in specified location. Only 1 item is required in the list. If multiple items are required, please separate it into multiple objective | `ContainerPickup{world=dungeon;x=120;y=4;z=263;item="{"v":3700,"type":"EMERALD_BLOCK"}"}` |          |
| world, x, y, z      | Location of the hopper                                                                                                                                                     |                                                                                           | true     |
| item                | Item required to pick up, type `/mg check` to get the formatted string                                                                                                     |                                                                                           | true     |
| fuzzy               | Is only item type and amount is checked or same item meta is required                                                                                                      | `true` or `false`                                                                         |          |
| remove              | Is the item being removed from the hopper or remains inside                                                                                                                | `true` or `false`                                                                         |          |

### Damage

<div align="left">

<figure><img src="../../.gitbook/assets/DamageObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters | Explanation                                                  | Examples                            | Required |
| ---------- | ------------------------------------------------------------ | ----------------------------------- | -------- |
| **Damage** | Times of damage required to take                             | `Damage{damage=10;raw=true;time=2}` |          |
| damage     | Minimum damage required to be counted                        | `1`                                 | true     |
| raw        | Is raw damage amount being counted or after damage reduction | `true` or `false`                   | true     |
| time       | Times of the damage to take                                  | `3`                                 | true     |

### **HasItem**

<div align="left">

<figure><img src="../../.gitbook/assets/HasItemObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters  | Explanation                                                                                                                                                   | Examples                                                                                                         | Required |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | -------- |
| **HasItem** | Items required to have in player's inventory. Only 1 item is required in the list. If multiple items are required, please separate it into multiple objective | `HasItem{allplayer=true;0='{"v":2865,"type":"REDSTONE_BLOCK"}';1='MythicMobs{id="SkeletonKingSword";amount=2}'}` |          |
| allplayer   | All players are required to have at lease 1 item in the list                                                                                                  | `true` or `false`                                                                                                |          |
| fuzzy       | Is only item type and amount is checked or same item meta is required                                                                                         | `true` or `false`                                                                                                |          |
| \<id>       | ID is meaningless, but it must be an integer. What items are required, type `/mg check` to get the formatted string                                           | `0='{"v":2865,"type":"REDSTONE_BLOCK"}';1='MythicMobs{id="SkeletonKingSword";amount=2}'`                         | true     |

### **LootChest**

<div align="left">

<figure><img src="../../.gitbook/assets/LootChestObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters    | Explanation                                                  | Examples          | Required |
| ------------- | ------------------------------------------------------------ | ----------------- | -------- |
| **LootChest** | Loot Chest required to open                                  | `LootChest{id=1}` |          |
| id            | ID of the loot chest, it should be declared `lootchests.yml` |                   | true     |

### Mob

| Parameters | Explanation                                                                                                       | Examples                                           | Required |
| ---------- | ----------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | -------- |
| **Mob**    | Mob required to kill, similar to [MythicMob](objective-list.md#mythicmob) but applicable to all type of mobs      | `Mob{name='Alpha Werewolf';namespace='elitemobs'}` |          |
| name       | Name of the mob, regex is supported                                                                               |                                                    | true     |
| namespace  | Namespace of the mob, some custom mob plugin might contain plugin-specific tag, it can be used for detection here |                                                    |          |

### **MythicMob (MythicMobs)**

<div align="left">

<figure><img src="../../.gitbook/assets/MythicMobObjecetive.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters    | Explanation                                                                                                    | Examples                                                                                                                                                                                                                                                                                          | Required |
| ------------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| **MythicMob** | MythicMobs mob required to kill, similar to [Mob](objective-list.md#mob) but only applicable to MythicMobs mob | `MythicMob{type=rat1;amount=3}`                                                                                                                                                                                                                                                                   |          |
| type          | Type of the MythicMob defined in `MythicMobs/Mobs/<yml contains the mob>.yml`                                  |                                                                                                                                                                                                                                                                                                   | true     |
| amount        | Amount of the mobs required to kill                                                                            | `3` if 3 of this mob is required to kill, the scoreboard shows `Mother Rat: 3`, `1` if only 1 is required to kill, the scoreboard shows `Mother Rat: 1`, if it is not set, the default amount is `1`, however, the scoreboard will show `Mother Rat: not dead` or `Mother Rat: dead` respectively |          |
| minlevel      | Minimum mobs level required to kill                                                                            |                                                                                                                                                                                                                                                                                                   |          |
| maxlevel      | Maximum mobs level required to kill                                                                            |                                                                                                                                                                                                                                                                                                   |          |

### NPCInteract (Citizens)

| Parameters      | Explanation                                                      | Examples                                      | Required |
| --------------- | ---------------------------------------------------------------- | --------------------------------------------- | -------- |
| **NPCInteract** | NPC required to interact by players                              | `NPCInteract{left=true;right=true;npcId="0"}` |          |
| id              | ID of the NPC declared in `MythicDungeons/groups/Ruins/npcs.yml` |                                               | true     |
| left            | Is left-clicking NPC accepted                                    | `true` or `false`                             |          |
| right           | Is right-clicking NPC accepted                                   | `true` or `false`                             |          |

### **PlayerPickup**

<div align="left">

<figure><img src="../../.gitbook/assets/PlayerPickupObjective.gif" alt="" width="540"><figcaption></figcaption></figure>

</div>

| Parameters       | Explanation                                                            | Examples                                                  | Required |
| ---------------- | ---------------------------------------------------------------------- | --------------------------------------------------------- | -------- |
| **PlayerPickup** | Item required to pick up by players                                    | `PlayerPickup{item='{"v":2865,"type":"REDSTONE_BLOCK"}'}` |          |
| item             | Item required to pick up, type `/mg check` to get the formatted string |                                                           |          |
| fuzzy            | Is only item type and amount is checked or same item meta is required  | `true` or `false`                                         |          |

### RedstonePower

| Parameters        | Explanation                                               | Examples                                                    | Required |
| ----------------- | --------------------------------------------------------- | ----------------------------------------------------------- | -------- |
| **RedstonePower** | Redstone power required for the specified block           | `RedstonePower{world=dungeon;x=115;y=5;z=247;min=1;max=15}` |          |
| world, x, y, z    | Location of the block to detect                           |                                                             | true     |
| min               | Minimum redstone power required to trigger this objective | `1` to `16`                                                 |          |
| max               | Maximum redstone power required to trigger this objective | `1` to `16`                                                 |          |
