# Loot Tables

Loot Tables is a collection of Sub-Tables, and Sub-Table is a collection of different items. Unlike regular item lines, you can define the weight of the Sub-Table so that the table with a higher weight has a bigger chance of being drawn, or even drawing a random amount of items in the list.

The items inside Sub-Table also have their own weight and amount when being drawn, the item with higher weight has a bigger chance of being drawn, and the amount of drawn item can be random between a range. Beware, if the item line has its own amount, the final amount will be multiplied by the drawn amount in the random range. The drawn items will be removed from the pool so that they will not be drawn again in this round.

If the items in the list do not fit in the draw amount, then only the items that fit in will be drawn. If you have 2 items in the list but the min & max amount is between 1 and 3, then the final amount of items being drawn will only be 1 or 2.

Loot Tables can be used in Loot Chest items declaration, you can simply add `- LootTable{id=Stage1Table} 1 2 3` where `Stage1Table` is the name of the Loot Table and `1 2 3` is the slot applying the Loot Table. If the items drawn do not fit in the slots, then the rear slots will not be filled or the items in the rear of the list will not be fitted in.

Loot Tables can also be used in Reward items declaration, you can simply add `- LootTable{id=Stage1Table}` where `Stage1Table` is the name of the Loot Table. Unlike Loot Chest, all of the items drawn will be given to players.

You can also use Loot Tables in Blacklisted Items declaration. Add `- LootTable{id=Stage1Table}`. However, unlike the usage above, all items in the Loot Table will be blacklisted and cannot be brought into the dungeon no matter the weight and min & max amount.

{% code title="Stage1Table.yml" lineNumbers="true" %}
```yaml
# ID of the loot table
Stage1Table:
  # ID of the sub-table, multiple sub-tables can be combined
  # First draw a sub-table, then draw items in sub-table
  ItemDropTable:
    # Weight of this sub-table, higher weight = higher chance being drawn
    # Chance of being drawn: <weight of this sub-table> / <total weight of all sub-tables>
    Weight: 1
    # Minimum amount of items will be drawn
    MinItems: 1
    # Maximum amount of items will be drawn
    MaxItems: 3
    # Items to draw
    # Use /mg check with the items on your hand to retrieve the string
    # The 1st parameter is the weight of this item is drawn
    # The 2nd parameter is the minimum amount of this item
    # The 3rd parameter is the maximum amount of this item
    #
    # The following has default weight of 1 and default amount of 1
    # {"v":2865,"type":"REDSTONE_BLOCK"}
    # The following has weight of 5 and default amount of 1 and exact 1
    # {"v":2865,"type":"REDSTONE_BLOCK"} 5
    # The following has weight of 5 and amount of 1 and exact 1
    # {"v":2865,"type":"REDSTONE_BLOCK"} 5 1
    # The following has weight of 5 and amounts between 1 and 64
    # {"v":2865,"type":"REDSTONE_BLOCK"} 5 1 64
    Items:
      - '{"v":2865,"type":"REDSTONE_BLOCK"} 1 1 64'
      - '{"v":2865,"type":"DIAMOND_BLOCK"} 1 1'
      - '{"v":2865,"type":"EMERALD_BLOCK"} 1 1'
  WeaponDropTable:
    Weight: 1
    MinItems: 1
    MaxItems: 3
    Items:
      - 'MMOItems{type=FOOD;id=ICE_CREAM;amount=64} 1 1'
      - 'MythicMobs{id="SkeletonKingSword";amount=2} 1 1'
```
{% endcode %}
