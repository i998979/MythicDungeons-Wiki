# Get Started

{% hint style="info" %}
**Reminder:** Unless specified, Dungeon Type will be named `Ruins` throughout the Wiki. Change it respectively.
{% endhint %}

There are multiple ways to create Dungeon Group depending on how the dungeon should be loaded.

Only 1 of the following methods should be chosen when creating a new Dungeon Group.

Follow [Build from scratch](get-started.md#build-from-scratch) if you:

* Want to start everything fresh and clean

Follow [With existing dungeon built in world](get-started.md#with-existing-dungeon-built-in-world) if you:

* Have a Dungeon built in world and want to use it

Follow [With pre-built schematic](get-started.md#with-pre-built-schematic) if you:

* Have a schematic file with the Dungeon you want to use

Follow [With all Dungeon Instances built in world](get-started.md#with-existing-dungeon-built-in-world) if you:

* Have all dungeon instances prebuilt in the world

{% hint style="info" %}
If all dungeon instances are prebuilt in the world, and `Length`, `Width`, and `Height` of the dungeon is defined, it is highly recommended to have `RestoreTerrains` disabled in `general.yml`. So that the terrain will not be unnecessarily restored. Beware of world interactions such as block breaking/placement or explosions, as the terrain is not restored.
{% endhint %}

However, it is still highly recommended to have a schematic file prepared or create Dungeon Group through `/mg creator` so that Dungeon dimensions and location are calculated automatically.

<details>

<summary><strong>Build from scratch:</strong></summary>

#### Preparing Dungeon

* Join the server
* Build a dungeon whatever you want (it does not have to be a cuboid, but it has to be selectable by 2 points)
* ![](https://user-images.githubusercontent.com/7139370/158058569-571a10b9-c7c2-42fb-b15a-c20d33199c7c.png)![](https://user-images.githubusercontent.com/7139370/158058574-38c7ae1e-db3b-4521-863f-c97990185873.png)

#### Creator Command

* Type `/mg creator` to start creating a new Dungeon Group
* Enter a unique Dungeon Group ID (no spaces)
* Enter a display name for the Dungeon Group

#### Select Dungeon Area

* Type `//wand` to get a WorldEdit wand
* Select 2 corners like this, the selected area should include everything in your dungeon
* ![](https://user-images.githubusercontent.com/7139370/158058831-96eb2715-11c5-4221-bc28-1f5fd14707bc.png)
* Type `//copy` to copy the Dungeon Area into WorldEdit's clipboard
* Type `done` to complete copying Dungeon area

The Creator Command will then save the area you have selected into clipboard, and it will be used for this Dungeon Group.

#### Defining Spawn Point

* Stand at the player Spawn Point of the dungeon, then type `add`
* Type `done` to complete defining player Spawn Point
* Type `done` again to save Dungeon Group

</details>

<details>

<summary><strong>With existing dungeon built in world:</strong></summary>

#### Preparing Dungeon

* Join the server
* Go to where your Dungeon is
* ![](https://user-images.githubusercontent.com/7139370/158058569-571a10b9-c7c2-42fb-b15a-c20d33199c7c.png)![](https://user-images.githubusercontent.com/7139370/158058574-38c7ae1e-db3b-4521-863f-c97990185873.png)

#### Creator Command

* Type `/mg creator` to start creating a new Dungeon Group
* Enter a unique Dungeon Group ID (no spaces)
* Enter a display name for the Dungeon Group

#### Select Dungeon Area

* Type `//wand` to get a WorldEdit wand
* Select 2 corners like this, the selected area should include everything in your dungeon
* ![](https://user-images.githubusercontent.com/7139370/158058831-96eb2715-11c5-4221-bc28-1f5fd14707bc.png)
* Type `//copy` to copy the Dungeon Area into WorldEdit's clipboard
* Type `done` to complete copying Dungeon area

The Creator Command will then save the area you have selected into clipboard, and it will be used for this Dungeon Group.

#### Defining Spawn Point

* Stand at the player Spawn Point of the dungeon, then type `add`
* Type `done` to complete defining player Spawn Point
* Type `done` again to save Dungeon Group

</details>

<details>

<summary><strong>With pre-built schematic:</strong></summary>

* Join the server
* Type `//schem load <Schematic Name>` to load schematic in WorldEdit/FastAsyncWorldEdit into clipboard
* Type `//paste` to place the schematic in world
* ![](https://user-images.githubusercontent.com/7139370/158058569-571a10b9-c7c2-42fb-b15a-c20d33199c7c.png)![](https://user-images.githubusercontent.com/7139370/158058574-38c7ae1e-db3b-4521-863f-c97990185873.png)

#### Creator Command

* Type `/mg creator` to start creating a new Dungeon Group
* Enter a unique Dungeon Group ID (no spaces)
* Enter a display name for the Dungeon Group

#### Select Dungeon Area

* Type `//wand` to get a WorldEdit wand
* Select 2 corners like this, the selected area should include everything in your dungeon
* Type `//copy` to copy the Dungeon Area into WorldEdit's clipboard
* Type `done` to complete copying Dungeon area

The Creator Command will then save the area you have selected into clipboard, and it will be used for this Dungeon Group.

#### Defining Spawn Point

* Stand at the player Spawn Point of the dungeon, then type `add`
* Type `done` to complete defining player Spawn Point
* Type `done` again to save Dungeon Group

</details>

<details>

<summary><del><strong>With all Dungeon Instances built in world:</strong></del></summary>

* ~~Join the server~~
* ~~Define `Row`, `Column`, `RowGap`, `ColumnGap` in `general.yml` depending on how many dungeon instances you want, total number of instances is `row * column`~~
* ~~Define `Length`, `Width`, `Height` of the dungeon schematic in `general.yml` depending on which corner the schematic is copied from. `Length` spans on z-axis positive, `Width` spans on x-axis positive, `Height` spans on y-axis positive. Use negative value if it spans oppositely~~
* ~~Paste the schematic in pre-defined dungeon instance location~~
* ~~Modify the files if needed~~
* ~~Type `/md reload group` to reload Dungeon Group~~

</details>

Dungeon Group is now loaded and ready for testing purposes. You will still need to define Objectives and Actions to make it playable.
