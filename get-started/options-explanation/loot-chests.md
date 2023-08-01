# Loot Chests

## **Under `Ruins.LootChests.<LootChest ID>`:**

| Parameters | Explanation                                                                                                                            | Examples                                                                                                                                                                |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Type       | Type of the loot chest                                                                                                                 | `CHEST` if the inventory type is a chest. It follows the rule from [Spigot API](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/inventory/InventoryType.html) |
| PerPlayer  | Whether other players have their own loot chest content or they share the same one                                                     | `true` or `false`                                                                                                                                                       |
| Renew      | How long in ticks will the loot chest renew                                                                                            |                                                                                                                                                                         |
| Items      | The item list of the loot chest, hold an item in-game, and type `/mg check` to get the formatted string, followed by the slot to place | `{"v":2865,"type":"REDSTONE_BLOCK"} 8` means adding a `REDSTONE_BLOCK` on slot `8`                                                                                      |
