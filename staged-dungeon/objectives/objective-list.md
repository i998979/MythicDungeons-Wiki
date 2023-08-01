# Objective List

## Under `Ruins.Stages.<ID>.Objectives`:

### **ChatMessage**

| Parameters      | Explanation                                                                              | Examples                                                                             | Required |
| --------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ | -------- |
| **ChatMessage** | Things required to say in chat in this stage                                             | `ChatMessage{message="hello world";scoreboard="greetings to the world";cancel=true}` |          |
| message         | Messages required to say, regular expressions are supported                              | `123[abc]456` for `123a456`, `123b456`, `123c456`                                    | true     |
| scoreboard      | Alternative text shown in scoreboard to avoid showing regular expressions directly on it |                                                                                      |          |
| cancel          | Is this message sent by the player not showing in chat                                   | `true` or `false`                                                                    |          |

### **Checkpoint**

| Parameters     | Explanation                                                           | Examples           | Required |
| -------------- | --------------------------------------------------------------------- | ------------------ | -------- |
| **Checkpoint** | Checkpoint required to reach in this stage                            | `Checkpoint{id=1}` |          |
| id             | ID of the checkpoint, it should be declared under `Ruins.Checkpoints` |                    | true     |
| allplayer      | Are all players required to stay inside the checkpoint                | `true` or `false`  |          |

### **HasItem**

| Parameters  | Explanation                                                                                                                                           | Examples                                                                                                         | Required |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | -------- |
| **HasItem** | Items required to have in this stage. Only 1 item is required in the list. If multiple items are required, please separate it into multiple objective | `HasItem{allplayer=true;0='{"v":2865,"type":"REDSTONE_BLOCK"}';1='MythicMobs{id="SkeletonKingSword";amount=2}'}` |          |
| allplayer   | All players are required to have at lease 1 item in the list                                                                                          | `true` or `false`                                                                                                |          |
| \<id>       | ID is meaningless, but it must be an integer. What items are required, type `/mg check` to get the formatted string                                   | `0='{"v":2865,"type":"REDSTONE_BLOCK"}';1='MythicMobs{id="SkeletonKingSword";amount=2}'`                         | true     |

### **LootChest**

| Parameters    | Explanation                                                         | Examples          | Required |
| ------------- | ------------------------------------------------------------------- | ----------------- | -------- |
| **LootChest** | Loot Chest required to open in this stage                           | `LootChest{id=1}` |          |
| id            | ID of the loot chest, it should be declared under `Ruins.LootChest` |                   | true     |

### **MythicMob**

| Parameters    | Explanation                                                                     | Examples                                                                                                                                                                                                                                                                                          | Required |
| ------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| **MythicMob** | MythicMobs mob required to kill in this stage                                   | `MythicMob{type=rat1;amount=3}`                                                                                                                                                                                                                                                                   |          |
| type          | Type of the MythicMob defined in `MythicMobs/Mobs/<Yml containing the mob>.yml` |                                                                                                                                                                                                                                                                                                   | true     |
| amount        | Amount of the mobs required to kill                                             | `3` if 3 of this mob is required to kill, the scoreboard shows `Mother Rat: 3`, `1` if only 1 is required to kill, the scoreboard shows `Mother Rat: 1`, if it is not set, the default amount is `1`, however, the scoreboard will show `Mother Rat: not dead` or `Mother Rat: dead` respectively |          |
| minlevel      | Minimum mobs level required to kill                                             |                                                                                                                                                                                                                                                                                                   |          |
| maxlevel      | Maximum mobs level required to kill                                             |                                                                                                                                                                                                                                                                                                   |          |

### **PlayerPickup**

| Parameters       | Explanation                                                            | Examples                                                  | Required |
| ---------------- | ---------------------------------------------------------------------- | --------------------------------------------------------- | -------- |
| **PlayerPickup** | Item required to pick up by players in this stage                      | `PlayerPickup{item='{"v":2865,"type":"REDSTONE_BLOCK"}'}` |          |
| item             | Item required to pick up, type `/mg check` to get the formatted string |                                                           |          |
