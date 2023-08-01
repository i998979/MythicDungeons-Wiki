# Migration Guide

## v1 to v2

As of MythicDungeons 2.0.0, Staged Dungeon System is created to expand the flexibility in creating more complicated dungeons and expand the flexibility in implementing new features. The whole dungeon flow including the way to spawn mobs create spawners, and checkpoint objectives have changed, the old way to create spawners, and bosses are deprecated and have been removed.

The logic behind is:

* Dungeon starts and does a list of actions
* Players completing different objectives
* List of actions will be done once the objectives of the stage are completed
* Start all branches(other stages) in the list
* Those branch stages do their list of actions
* and so on...

By using the staged dungeon system, you may

* Create a complicated dungeon, different decisions the player make can lead to different branch with different results
* Have a greater understanding in how the dungeon runs, it is basically `Actions` -> player complete `Objectives` -> completion `Actions`

To help transition these changes here is some useful information.

By typing `/mg migrate <file name/all>`, the dungeon specified will be migrated. To migrate all dungeon configurations, you may enter `all` in the command argument.

Alternatively, if you find the migrated configuration does not fit you or it is not working, you may refer to this picture and do the migration manually.&#x20;

<figure><img src="https://user-images.githubusercontent.com/7139370/179409327-36ea4331-2422-4a9e-822c-feed78ed3f02.png" alt=""><figcaption></figcaption></figure>
