# Dungeon Group Config

{% hint style="warning" %}
**Warning:** The sample config is purely for reference only. Do not copy & paste, change the parameters like location, and mob type accordingly.
{% endhint %}

Dungeon Group is the type of dungeon, all the dungeon instances share the same arguments. But dungeon-specific arguments like origin, and player spawns are automatically calculated.

As of MythicDungeons 3.0.0, Dungeon Group Config has been split into multiple config files. This would provide a bigger flexibility for future updates.

The minimum file structure for a working dungeon is as follows:

* Ruins/
  * schematics/
    * Ruins.schem
  * [general.yml](general.yml.md)
  * [stages.yml](stages.yml.md)

In the following example, the following items are required for the dungeon to work.

* A world named `dungeon`
* `Ruins.schem` located inside `Ruins/schematics`
* MythicMob `SkeletalKnight` declared in MythicMobs

Additionally, different config files can be added to expand the content of the dungeon.
