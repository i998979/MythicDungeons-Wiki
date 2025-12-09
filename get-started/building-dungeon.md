# Building Dungeon

{% hint style="info" %}
**Reminder:** Unless specified, Dungeon Type will be named `Ruins` throughout the Wiki. Change it respectively.
{% endhint %}

Since 3.2.2-BETA, a convenient `/mg creator` command has been made to simplify Dungeon Group creation. Dungeon instances will automatically be calculated and spanned on x-axis positive and z-axis positive. It is highly recommended to do it in an empty world to avoid damaging existing terrains.

If all dungeon instances are prebuilt in the world, defining `Length`, `Width`, and `Height` of the dungeon and have `RestoreTerrains` disabled in `general.yml` so that the terrain will not be unnecessarily restored. Beware of world interactions like block breaking/placement, or explosions, as the terrain is not restored.

However, it is still highly recommended to have a schematic file in place or create Dungeon Group through `/mg creator` so that the plugin calculates things like location automatically.

Only 1 of the following method should be chosen when creating a new Dungeon Group.

{% tabs %}
{% tab title="Define in-game" %}


* Join the server
* Build a dungeon whatever you want (it does not need to be a cuboid, but it has to be selectable by 2 points)

![](https://user-images.githubusercontent.com/7139370/158058569-571a10b9-c7c2-42fb-b15a-c20d33199c7c.png)![](https://user-images.githubusercontent.com/7139370/158058574-38c7ae1e-db3b-4521-863f-c97990185873.png)

#### Creator Command

* Type `/mg creator` to start creating a new Dungeon Group, type `cancel` to cancel at any time
* Enter a unique Dungeon Group ID (no spaces)
* Enter a display name for the Dungeon Group

#### Select Dungeon Area

* Type `//wand` to get a WorldEdit wand
* Select 2 corners like this, the selected area should include everything in your dungeon

![](https://user-images.githubusercontent.com/7139370/158058831-96eb2715-11c5-4221-bc28-1f5fd14707bc.png)

* Type `//copy` to copy the Dungeon Area into clipboard
* Type `done` to complete copying Dungeon Area

#### Defining Spawn Point

* Stand at the player Spawn Point of the dungeon, then type anything
* Type done to complete defining player Spawn Point
* Type `done` to save Dungeon Group

Dungeon Group is now loaded and ready for testing purposes. You will still need to define Objectives and Actions to make it playable.
{% endtab %}

{% tab title="With schematic file" %}
* Join the server
* Build a dungeon whatever you want (it does not need to be a cuboid, but it has to be selectable by 2 points)

![](https://user-images.githubusercontent.com/7139370/158058569-571a10b9-c7c2-42fb-b15a-c20d33199c7c.png)![](https://user-images.githubusercontent.com/7139370/158058574-38c7ae1e-db3b-4521-863f-c97990185873.png)

#### Creating schematic

* Type `//wand` to get a WorldEdit wand
* Select 2 corners like this, the selected area should include everything in your dungeon

![](https://user-images.githubusercontent.com/7139370/158058831-96eb2715-11c5-4221-bc28-1f5fd14707bc.png)

* Stand at the corner of the dungeon, type `//copy`, then `//schem save Ruins`

<img src="https://user-images.githubusercontent.com/7139370/158059158-9a46642e-db57-41ea-914d-cd3eeb4e02d8.png" alt="" data-size="original">

* Do not move, remember the location, this will be the `Origin` of the dungeon
* Locate `WorldEdit/schematics` or `FastAsyncWorldEdit/schematics`, find the `Ruins.schem`
* Copy the `Ruins.schem` to `MythicDungeons/Ruins/schematics`
* Modify the files if needed
* Type `/md reload group` to reload Dungeon Group
{% endtab %}

{% tab title="Define size manually" %}
* Join the server
* Define `Row`, `Column`, `RowGap`, `ColumnGap` in `general.yml` depending on how many dungeon instances you want, total number of instances is `row * column`
* Define `Length`, `Width`, `Height` of the dungeon schematic in `general.yml` depending on which corner the schematic is copied from. `Length` spans on z-axis positive, `Width` spans on x-axis positive, `Height` spans on y-axis positive. Use negative value if it spans oppositely
* Paste the schematic in pre-defined dungeon instance location
* Modify the files if needed
* Type `/md reload group` to reload Dungeon Group
{% endtab %}
{% endtabs %}
