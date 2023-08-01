# Building Dungeon

Since 2.2.2-SNAPSHOT, schematic file is no longer hard-dependency if you have all 3 dimensions `Length`, `Width`, and `Height` configured. It provides a possibility to use the plugin with the dungeon pre-built in the world.

However, it is still highly recommended to have a schematic file in place so that the plugin calculates things like location automatically.

Also, it is recommended to have `RestoreTerrains` in `config.yml` disabled if have a huge dungeon and you do not allow players to break/place blocks, explosions, etc. In this case, you should have all dungeon instances pasted in the world already and all 3 dimensions configured.

{% hint style="info" %}
**Reminder:** Unless specified, Dungeon Group ID will be named  `Ruins` throughout the Wiki. Change it respectively.
{% endhint %}

{% tabs %}
{% tab title="With schematic file" %}
* Join the server
* Build a dungeon whatever you want, for example, my dungeon looks like this\
  (It does not need to be a cuboid but it has to be selectable by 2 points)

![](https://user-images.githubusercontent.com/7139370/158058569-571a10b9-c7c2-42fb-b15a-c20d33199c7c.png)![](https://user-images.githubusercontent.com/7139370/158058574-38c7ae1e-db3b-4521-863f-c97990185873.png)

#### Creating schematic

* Type `//wand` to get a WorldEdit wand
* Select 2 corners like this, the selected area should include everything in your dungeon

![](https://user-images.githubusercontent.com/7139370/158058831-96eb2715-11c5-4221-bc28-1f5fd14707bc.png)

* Stand at the corner of the dungeon, type `//copy`, then `//schem save <Dungeon ID of this dungeon>`

<img src="https://user-images.githubusercontent.com/7139370/158059158-9a46642e-db57-41ea-914d-cd3eeb4e02d8.png" alt="" data-size="original">

* Do not move, remember the location, this will be the `Origin` of this dungeon, we will need this later
* Locate `WorldEdit/schematics` or `FastAsyncWorldEdit/schematics`, find the `<Dungeon ID of this dungeon>.schem` you just created
* Copy the `<Dungeon ID of this dungeon>.schem` to `MythicDungeons/schematics`
{% endtab %}

{% tab title="Without schematic file" %}
* Join the server
* Define `Row`, `Column`, `RowGap`, `ColumnGap` in `Ruins.yml` depending on how many dungeon instances you want, total amount of instances is row \* column
* Define `Length`, `Width`, `Height` of the dungeon schematic in `Ruins.yml` depending on which corner the schematic is copied from. `Length` spans on z-axis positive, `Width` spans on x-axis positive, `Height` spans on y-axis positive. Use negative value if it spans oppositely
* Paste the schematic file into `MythicDungeons/schematics`
{% endtab %}
{% endtabs %}
