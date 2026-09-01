# Dungeon Group Config

{% hint style="warning" %}
**Warning:** The sample config is purely for reference only. Do not copy & paste, change the parameters such as location, and mob type accordingly.
{% endhint %}

After following the guide in [Get Started](../get-started.md), you should have a runnable Dungeon with no content. Now it is time to add some content to it.

To begin with, we will be focusing on `general.yml` and `stages.yml`.

In the [`general.yml (Simplified)`](general.yml.md#general-config-simplified) and [`stages.yml (Simplified)`](stages.yml.md#stages-simplified) sample config, the following prerequisites are required for the dungeon to work.

* A world named `dungeon`
* MythicMob `SkeletalKnight` declared in MythicMobs

`general.yml` configures general parameters of the Dungeon Group, like how many players can join, how many dungeon instances can exist at the same time, dungeon challenge time, and player spawns, etc...

`stages.yml` configures your main dungeon gameplay, how your dungeon progresses, which mobs to kill, checkpoints to reach, etc... More information can be found in [Staged Dungeon](https://app.gitbook.com/s/hiyaLQEIUITeccgpzZh2/staged-dungeon).
