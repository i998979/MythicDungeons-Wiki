# Room Mechanics

{% hint style="info" %}
**Reminder:** If you are not using any supported external party plugin or its plugin hook is not enabled, the internal room implementation is used instead. When the room disbands, all members will be removed.
{% endhint %}

## **Regular Room**

If you are using any supported external party plugin and its plugin hook is enabled, the room created by `/mr menu` or `/mr create` will automatically import party members upon room creation. You can invite/remove room members or promote someone to owner from either external party plugin or MythicDungeons.

However, disbanding the room does not disband the party, disbanding the party does not disband the room.

If a party joins an existing room, 2 parties will be merged, and the room owner will be the party owner.

External party plugin's party owner and members will be synchronized with the room every 1 second. New owner will be promoted, old owner will be demoted, members removed by any supported party plugin will be kicked from the room, and members added by external party plugin will be added to the room.

## **Temporary Room**

Using Join Sign or Join NPC creates a temporary room. It acts like a queue with a fixed size. If you are using any supported external party plugin and its plugin hook is enabled, the party will be put into a temporary room that can fit all party members in, or create a new temporary room if no existing room with enough space, parties will not be merged.

The dungeon will auto-start after countdown if the room has enough players. However, the auto-start will be cancelled if there are insufficient players.

## **Queue Command**

Queue Command acts the same as Join Sign or Join NPC, it creates a temporary room and acts like a queue with a fixed size as well. However, Dungeon Group type wanted to queue for has to be specified. The command is `/mr queue <Type>`.
