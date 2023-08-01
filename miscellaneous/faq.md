# FAQ

{% hint style="info" %}
Can't answer your question? Please tell me and I will answer you as soon as possible.
{% endhint %}

## General

<details>

<summary><strong>I found bugs / console errors.</strong></summary>

Try to download the plugin again before asking for help. I will help as much as I can if you provide enough information such as error logs, how to reproduce the error. Please PM me or leave a comment in the Discussion Section. Otherwise, I will ignore you.

</details>

<details>

<summary><strong>Nothing was received after typing the command.</strong></summary>

Please make sure that you follow the format before executing the command. You might get nothing if you enter the wrong arguments. Also, please make sure that the plugin is loaded and doesn't conflict with other plugins. You may ask for help but I can't promise I can fix the error if the error is not produced by my plugin.

</details>

<details>

<summary><strong>Does this plugin support xxx Platform / xxx Server / xxx Minecraft version?</strong></summary>

If you are having problems with the specified Platform / Server / Minecraft version, please PM me or leave a comment in the Discussion Section. I will try to fix it. However, there is no guarantee that it will work.

</details>

## Plugin-specific

<details>

<summary>The scoreboard does not show when the dungeon starts.</summary>

If you have TAB installed, disable it in the dungeon world.&#x20;

</details>

<details>

<summary>Loot Chest does not spawn even if it is configured correctly.</summary>

Loot Chest does not spawn by default, it requires you to have the chest in the schematic and requires to be enabled through [Loot Chest Action](https://factorycraft.gitbook.io/wiki/get-started/actions-completions-and-fail-actions/action-list#lootchest).

</details>

<details>

<summary>MythicMobs Spawner keeps spawning mobs.</summary>

MythicMobs Spawner start spawning mobs once it is called, it is default enabled, you may disable it whenever you want through [MythicSpawner Action](https://factorycraft.gitbook.io/wiki/get-started/actions-completions-and-fail-actions/action-list#mythicspawner).

</details>

<details>

<summary>How to customize Dungeon Group icon?</summary>

An external item editing plugin is required or use an Anvil instead.

Edit the name, lore, custom model data through external item editing plugin, then type `/mg check` and click the message to copy formatted string, and paste it into the [Dungeon Group Config](../configuration/dungeon-group-config-simplified.md).

</details>

<details>

<summary>Unwanted items are dropped on ground everywhere.</summary>

Please make sure that the dungeon instance does not overlap with any existing builds.

</details>

<details>

<summary>Players get teleported outside during dungeon fight.</summary>

Please make sure that other plugins did not handle teleport upon death / login.

</details>

<details>

<summary>Getting <code>java.lang.NullPointerException: Cannot invoke "org.bukkit.World.getName()</code> when loading.</summary>

Most likely you have a custom world generator and / or the world wasn't registered when the plugin loads. Try enabling `LoadDelay` in [General Config](../configuration/general-config.md).

</details>

<details>

<summary>Getting <code>java.lang.IndexOutOfBoundsException</code> when starting dungeon.</summary>

The dungeon schematic is most likely pasting outside Minecraft's height limit. Try adjusting `Origin` in[ Dungeon Group Config](../configuration/dungeon-group-config-simplified.md).

</details>

<details>

<summary>Getting <code>Caused by: java.lang.NoClassDefFoundError</code>.</summary>

Please make sure that all dependencies are installed properly.

If you have plugin hook enabled, please make sure those plugins are installed properly.

Otherwise, disable the plugin hook that you don't have the plugin installed.

</details>
