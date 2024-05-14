# Migration Guide

## v2 to v3

The Dungeon Group file structure has changed since MythicDungeons 3.0.0 in order to provide a bigger flexibility for future updates.

* In-Game Scoreboard is renamed to Scoreboard Display and has been moved into Stages along with BossBar Display and Action Bar Display
* Price is renamed to Requirement to cope with PlaceholderAPI condition check support
* Moved various global configuration settings to dungeon-specific

By typing `/mg migrate <file name/all>`, the dungeon specified will be migrated. To migrate all dungeon configurations, you may enter `all` in the command argument.

~~Alternatively, if you find the migrated configuration does not fit you or it is not working, you may refer to this picture and migrate manually.~~&#x20;

## v1 to v2

As of MythicDungeons 2.0.0, Staged Dungeon System is created to expand the flexibility in creating more complicated dungeons and expand the flexibility in implementing new features. The whole dungeon flow including the way to spawn mobs create spawners, and checkpoint objectives has changed, the old way to create spawners, and bosses is deprecated and has been removed.

The logic behind is:

* Dungeon starts and does a list of actions
* Players completing different objectives
* List of actions will be done once the objectives of the stage are completed
* Start all branches(other stages) in the list
* Those branch stages do their list of actions
* and so on...

By using the staged dungeon system, you may

* Create a complicated dungeon, different decisions the player makes can lead to different branches with different results
* Have a greater understanding of how the dungeon runs, it is basically `Actions` -> player complete `Objectives` -> completion `Actions`

To help transition these changes here is some useful information.

By typing `/mg migrate <file name/all>`, the dungeon specified will be migrated. To migrate all dungeon configurations, you may enter `all` in the command argument.

Alternatively, if you find the migrated configuration does not fit you or it is not working, you may refer to this picture and migrate manually.&#x20;

<figure><img src="https://user-images.githubusercontent.com/7139370/179409327-36ea4331-2422-4a9e-822c-feed78ed3f02.png" alt=""><figcaption></figcaption></figure>
