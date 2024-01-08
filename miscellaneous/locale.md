# Locale

{% hint style="info" %}
**Reminder:** This page might not be updated regularly. You may check the changelog on the resource page or inside the downloaded jar.

Please let me know if you need additional placeholders.
{% endhint %}

## General Messages (en\_US.yml)

For General chat messages, you may create a new yml file and modify the content. Then change the `Language` in `config.yml`.

{% code title="en_US.yml" lineNumbers="true" %}
```yaml
#
# Common general message
#
PREFIX: "&e[&bMythicDungeons&e]&r "
MESSAGE_NO_PERMISSION: "&cYou don't have permission to perform this command."
MESSAGE_NOT_PLAYER: "&cYou must be a player to execute this command."
MESSAGE_PLAYER_NOT_FOUND: "&cPlayer named {0} not found."
MESSAGE_PLAYER_OFFLINE: "&cPlayer {0}&c is not online."
MESSAGE_CHAT_ENTER_MESSAGE: "&cPlease enter the message."
MESSAGE_ENTER_OWN_NAME: "&cYou cannot enter your name."
MESSAGE_PAGE_INVALID: "&cThe page number you have entered is invalid."


#
# Common Room message
#
MESSAGE_ROOM_NOT_IN_ROOM: "&cYou are not in any room."
MESSAGE_ROOM_ALREADY_IN: "&cYou are already in a room."
MESSAGE_ROOM_PLAYER_NOT_IN: "&cPlayer {0}&c is not in your room."
MESSAGE_ROOM_PLAYER_ALREADY_IN: "&cPlayer {0}&c is already in your room."
MESSAGE_ROOM_COMMAND_UNAVAILABLE: "&cThis command is unavailable."
MESSAGE_ROOM_NOT_OWNER: "&cYou are not room owner."
MESSAGE_ROOM_ID_INVALID: "&cRoom with id {0} not found."
MESSAGE_ROOM_NOT_EXIST: "&cThe room does not exist."
MESSAGE_ROOM_FULL: "&cThe room is already full."
MESSAGE_ROOM_START_MAX: "&cDungeon cannot be started because the room has more than {0} players. (Current: {1})."
MESSAGE_ROOM_START_MIN: "&cDungeon cannot be started because the room has less than {0} players. (Current: {1})."
MESSAGE_ROOM_OFFLINE_OWNER: "&cThe owner is not online. Tell him/her to get online!"
MESSAGE_ROOM_OFFLINE_MEMBER: "&c1 member is not online. Tell him/her to get online!"
MESSAGE_ROOM_OFFLINE_MEMBERS: "&c{0} members are not online. Tell them to get online!"

# Chat
MESSAGE_ROOM_CHAT: "&5[&6Room&5]&r {0}&r: {1}"

# View
MESSAGE_ROOM_VIEWING: "&aViewing {0}&a's {1}&a room."
MESSAGE_ROOM_VIEW_NON_PUBLIC: "&aYou cannot view this room as it is not public."

# Invite
MESSAGE_ROOM_INVITE_ENTER_NAME: "&cPlease enter the player's name who has sent you the invitation."
MESSAGE_ROOM_INVITE_NO_INVITATION: "&cYou don't have an invitation from {0}&c."
MESSAGE_ROOM_INVITE_DECLINED_INVITER: "&e{0}&e has declined your invitation."
MESSAGE_ROOM_INVITE_DECLINED_SELF: "&eYou declined {0}&e room invitation by {1}&e."
MESSAGE_ROOM_INVITE_PLAYER: "&cPlease enter player's name you want to invite."
MESSAGE_ROOM_INVITE_ALREADY_INVITED: "&c{0}&c is already invited to the room. Please wait until he/she accepts."
MESSAGE_ROOM_INVITE_OTHERS: "&e{0}&e has invited {1}&e to the room."
MESSAGE_ROOM_INVITE_RECEIVED: "&e{0}&e invited you to a {1}&e room. Type /room accept {0} to accept the invitation."
MESSAGE_ROOM_INVITE_REMOVED: "&cThe invitation sent to {0}&c has been removed."
MESSAGE_ROOM_INVITE_INVALID: "&cThe invitation sent to {0}&c does not exist or expired."
MESSAGE_ROOM_INVITE_EXPIRED_INVITER: "&eThe invitation of {0} &esent to {1} &ehas been expired."
MESSAGE_ROOM_INVITE_EXPIRED_INVITED: "&eThe invitation of {0} &esent from {1} &ehas been expired."

# Join
MESSAGE_ROOM_JOIN_SELF: "&eYou have joined the room with id {0} owned by {1}&e."
MESSAGE_ROOM_JOIN_SELF_NO_OWNER: "&eYou have joined the room with id {0}."
MESSAGE_ROOM_JOIN_MEMBER: "&e{0}&e has joined the room."
MESSAGE_ROOM_JOIN_ENTER_NAME_OR_ID: "&cPlease enter the room owner's name or room ID that you want to join."
MESSAGE_ROOM_JOIN_NO_OWNED: "&c{0}&c does not own any rooms."
MESSAGE_ROOM_JOIN_ENTER_PASSWORD: "&cPlease enter the password of the room by typing /room join {0} <Password>."
MESSAGE_ROOM_JOIN_PASSWORD_INCORRECT: "&cIncorrect password."
MESSAGE_ROOM_JOIN_PRIVATE: "&cThe room you are joining is private and you don't have an invitation."
MESSAGE_ROOM_STARTED: "&cThe room has already started."

# Join Temp
MESSAGE_ROOM_JOIN_NOT_OWNER: "&cYou must be room owner to do this."
MESSAGE_ROOM_JOIN_NO_ROOM: "&cThere is no room to join at the moment. (current: {0}, max: {1})"
MESSAGE_ROOM_JOIN_NOT_IN_ROOM: "&cYou must be in a room to do this."
MESSAGE_ROOM_AUTOSTART_INSUFFICIENT_PLAYER: "&cInsufficient players, autostart cancelled. (required: {0}, current: {1})"
MESSAGE_ROOM_AUTOSTART_COUNTDOWN: "&eDungeon {1} &eis starting in {0} s."

# All invite
MESSAGE_ROOM_ALLINVITE_ENABLED: "&e{0}&a enabled&e all invite. Now all members can invite players."
MESSAGE_ROOM_ALLINVITE_DISABLED: "&e{0}&c disabled&e all invite. Members can no longer invite new players."

# Create
MESSAGE_ROOM_CREATED: "&eCreated room for dungeon {0}&e."
MESSAGE_ROOM_NO_PERMISSION_CREATE: "&cYou don't have permission to create room for dungeon {0}&c."
MESSAGE_ROOM_NO_PERMISSION_JOIN: "&cYou don't have permission to join room for dungeon {0}&c."
MESSAGE_ROOM_NOT_LEADER: "&cYou are not party leader."

# Disband
MESSAGE_ROOM_DISBAND_SELF: "&eYou disbanded the room."
MESSAGE_ROOM_DISBAND_MEMBER: "&e{0}&e has disbanded the room."
MESSAGE_ROOM_DISBAND_LEFT_SELF: "&eYou have left the room and the room is disbanded."
MESSAGE_ROOM_DISBAND_LEFT_MEMBER: "&eThe room owner has left the room and the room is disbanded."

# Leave
MESSAGE_ROOM_LEFT_SELF: "&eYou left the room."
MESSAGE_ROOM_LEFT_MEMBER: "&e{0}&e left the room."

# Note
MESSAGE_ROOM_NOTE_CLEARED: "&eRoom note has been cleared."
MESSAGE_ROOM_NOTE_SET: "&eRoom note has been set to \"{0}\"."

# Privacy
MESSAGE_ROOM_PRIVACY: "&cPlease enter room privacy. (Available options: PUBLIC/PRIVATE/PASSWORD)"
MESSAGE_ROOM_PRIVACY_ENTER_NEW_PASSWORD: "&cPlease enter the new password."
MESSAGE_ROOM_PRIVACY_EMPTY_PASSWORD: "&cEmpty password entered. Nothing changed."

MESSAGE_ROOM_PRIVACY_PASSWORD_SELF: "&eRoom privacy has set to &a{0}&e with password \"&7{1}&e\"."
MESSAGE_ROOM_PRIVACY_UPDATED: "&eRoom privacy has set to &a{0}&e."

# Promote
MESSAGE_ROOM_PROMOTE_ENTER_NEW_OWNER: "&cPlease enter new owner's name."
MESSAGE_ROOM_PROMOTED_NEW_OWNER: "&eYou have been promoted to room owner."
MESSAGE_ROOM_PROMOTED_MEMBER: "&e{0}&e has been promoted to room owner."

# Remove
MESSAGE_ROOM_REMOVE_NAME: "&cPlease enter player's name to remove."
MESSAGE_ROOM_REMOVE_SELF: "&cYou removed yourself and the room is disbanded."
MESSAGE_ROOM_REMOVE_REMOVED: "&eYou have been removed from {0}&e's room."
MESSAGE_ROOM_REMOVE_OWNER: "&eYou removed {0}&e from the room."
MESSAGE_ROOM_REMOVE_MEMBER: "&eMember {0}&e has been removed from the room."


#
# Common DungeonGroup message
#
MESSAGE_GROUP_ENTER_TYPE: "&cPlease enter a Dungeon group type."
MESSAGE_GROUP_TYPE_NOT_EXIST: "&cDungeon group type {0} does not exist."
MESSAGE_GROUP_TYPE_ALREADY_EXIST: "&cDungeon group type {0} already exist."
MESSAGE_GROUP_ENTER_DISPLAY_NAME: "&cPlease enter dungeon group display name."
MESSAGE_GROUP_CREATED: "&aDungeon group type {0} named {1}&a was created."
MESSAGE_GROUP_DELETED: "&aDungeon group type {0} was deleted."
MESSAGE_GROUP_CANNOT_LOAD_STILL_RUNNING: "&cDungeon groups cannot be loaded since there are dungeons still running."
MESSAGE_GROUP_FILE_NOT_EXIST: "&aDungeon group file {0} does not exist."
MESSAGE_GROUP_LOADED: "&aDungeon group {0} loaded from config."
MESSAGE_GROUPS_LOADED: "&aDungeon groups loaded from config."
MESSAGE_GROUP_SAVED: "&aDungeon group {0} saved into config."
MESSAGE_GROUPS_SAVED: "&aDungeon groups saved into config."
MESSAGE_GROUP_ENABLED: "&aDungeon group type {0} is enabled."
MESSAGE_GROUP_DISABLED: "&cDungeon group type {0} is disabled."

MESSAGE_GROUP_MIGRATE_ENTER_NAME: "&cPlease enter a file name to migrate."
MESSAGE_GROUP_MIGRATE_NOT_EXIST: "&cThe file you have entered does not exist."
MESSAGE_GROUP_MIGRATE_ALL: "&aMigrating all dungeon groups..."
MESSAGE_GROUP_MIGRATE_COMPLETE_ALL: "&aCompleted migration for all dungeon groups."
MESSAGE_GROUP_MIGRATE_FAIL_SOME: "&cSome of the dungeon group failed to migrate. Please check the server console for details."
MESSAGE_GROUP_MIGRATE_COMPLETE: "&aCompleted migration for dungeon group {0}."
MESSAGE_GROUP_MIGRATE_FAIL: "&cFailed to migrate dungeon group {0}."


#
# Common Dungeon message
#
MESSAGE_DUNGEON_NOT_IN_DUNGEON: "&cYou are not in any dungeon."
MESSAGE_DUNGEON_ALREADY_IN_RUN: "&cOne/some member(s) already in a dungeon run."
MESSAGE_DUNGEON_ALREADY_IN_RUN_SELF: "&cYou are already in a dungeon run."
MESSAGE_DUNGEON_BLACKLIST_ITEM: "&cBlacklisted item {0} was found in one/some member(s) inventory."
MESSAGE_DUNGEON_BLACKLIST_ITEM_SELF: "&cBlacklisted item {0} was found in your inventory."

MESSAGE_DUNGEON_CHAT: "&5[&6Dungeon&5]&r {0}&r: {1}"

MESSAGE_DUNGEON_LIMIT_REACHED: "&cDungeon {0}&c limit has reached. Please join an existing one or wait for one of them to finish."

MESSAGE_DUNGEON_ENTER_ID: "&cPlease enter dungeon's id."
MESSAGE_DUNGEON_ID_INVALID: "&cThe dungeon's id you have entered is invalid."
MESSAGE_DUNGEON_ID_NOT_EXIST: "&cThe dungeon's id you have entered does not exist."

MESSAGE_DUNGEON_NO_PERMISSION_CREATE: "&cYou don't have permission to create dungeon {0}&c."
MESSAGE_DUNGEON__NO_PERMISSION_JOIN: "&cOne/some member(s) does not have permission to join dungeon {0}&c."
MESSAGE_DUNGEON__NO_PERMISSION_JOIN_SELF: "&cYou don't have permission to join dungeon {0}&c."
MESSAGE_DUNGEON_GROUP_DISABLED: "&cDungeon {0} is disabled."

# Player removal message
MESSAGE_DUNGEON_PLAYER_NAME_TO_REMOVE: "&cPlease enter player's name to remove."
MESSAGE_DUNGEON_PLAYER_REMOVED: "&aPlayer {0}&a has been removed from the dungeon."
MESSAGE_DUNGEON_PLAYER_BE_REMOVED: "&cYou have been removed from the dungeon."
MESSAGE_DUNGEON_PLAYER_LEAVE_SELF: "&aYou have left the dungeon."
MESSAGE_DUNGEON_OFFLINE_PLAYER: "&c1 challenger is not online, tell him/her to get online."
MESSAGE_DUNGEON_OFFLINE_PLAYERS: "&c{0} challengers are not online, tell them to get online."

# Join message
MESSAGE_DUNGEON_NO_AVAILABLE: "&cThere is no dungeon {0}&c available at the moment. Please create a new one or try again later."
MESSAGE_DUNGEON_ALREADY_STARTED: "&cDungeon {0}&c with id {1} has already started."
MESSAGE_DUNGEON_NOT_RUNNING: "&cDungeon {0}&c with id {1} is not running."
MESSAGE_DUNGEON_ALREADY_STOPPED: "&cDungeon {0}&c with id {1} has already stopped."
MESSAGE_DUNGEON_ALREADY_JOINED: "&eYou have already joined the dungeon {0}&e with id {1}."
MESSAGE_DUNGEON_JOINED: "&eYou have joined the dungeon {0}&e with id {1}."
MESSAGE_DUNGEON_STARTED_OWNER: "&eYou have started the dungeon {0}&e with id {1}."
MESSAGE_DUNGEON_STARTED_MEMBER: "&e{0}&e has started the dungeon {1}&e with id {2}."
MESSAGE_DUNGEON_START_CANCELLED_OWNER: "&cYou have cancelled the start of the dungeon."
MESSAGE_DUNGEON_START_CANCELLED_MEMBER: "&cRoom owner cancelled the start of the dungeon."
MESSAGE_DUNGEON_CANNOT_CREATE: "&cDungeon {0} &ccannot be created."
MESSAGE_DUNGEON_CANNOT_CREATE_DISABLED: "&cDungeon {0} &ccannot be created because it is disabled."
MESSAGE_DUNGEON_CANNOT_AFFORD: "&cOne/some member(s) cannot afford the price."

# Admin message
MESSAGE_DUNGEON_LOADED: "&aDungeons loaded."
MESSAGE_DUNGEON_SAVED: "&aDungeons saved."
MESSAGE_DUNGEON_CREATED: "&aCreated dungeon {0}&a with id {1}."
MESSAGE_DUNGEON_STARTED: "&aStarted dungeon {0}&a with id {1}."
MESSAGE_DUNGEON_STOPPED: "&aStopped dungeon {0}&a with id {1}."


#
# Title
#
TITLE_COUNTDOWN_3: "&e❸"
TITLE_COUNTDOWN_2: "&6❷"
TITLE_COUNTDOWN_1: "&c❶"
TITLE_COUNTDOWN_0: "&fFIGHT!"


#
# Miscellaneous
#
MESSAGE_DUNGEON_PLAYTIME_COUNTDOWN: "&aDungeon {0} is ending in {1}s."

MESSAGE_DUNGEON_FAIL_EXPIRED: "&cDungeon challenge failed. The timer has expired."
MESSAGE_DUNGEON_FAIL_DEATH: "&cDungeon challenge failed. The death limit has been reached."
MESSAGE_DUNGEON_COMPLETED: "&5Congratulation! You have completed dungeon {0}&5 !"

MESSAGE_DUNGEON_BUFF_CLAIMABLE: "§aBuff {0} is now claimable."

MESSAGE_DUNGEON_TELEPORT_RUNNING: "&2You have been teleported to dungeon spawn as the dungeon you have joined is still running."
MESSAGE_DUNGEON_TELEPORT_RUNNING_INVALID: "&2You have been teleported to dungeon spawn as the dungeon you have joined is still running and your logout location is invalid."
MESSAGE_DUNGEON_TELEPORT_PREVIOUS: "&2You have been teleported to your previous location as the dungeon you have joined is still running."
MESSAGE_DUNGEON_TELEPORT_CHECKPOINT: "&2You have been teleported to your checkpoint {0}&2 as the dungeon you have joined is still running."

MESSAGE_DUNGEON_RESPAWN: "&aYou have respawned in dungeon's spawn."
MESSAGE_DUNGEON_RESPAWN_CHECKPOINT: "&aYou have respawned in {0}&a."

MESSAGE_DUNGEON_COMMAND_BLOCKED: "&cYou are not allowed to use this command during dungeon fight."


#
# Scoreboard
#
SCOREBOARD_STATUS_WAITING: "Waiting"
SCOREBOARD_STATUS_STARTING_SECOND: "Starting in {0} s"

SCOREBOARD_INGAME_CHATMESSAGE_YES: "&aYes"
SCOREBOARD_INGAME_CHATMESSAGE_NO: "&cNo"
SCOREBOARD_INGAME_CHECKPOINT_NOT_REACHED: "&cNot reached"
SCOREBOARD_INGAME_CHECKPOINT_REACHED: "&aReached"
SCOREBOARD_INGAME_HASITEM_YES: "&aYes"
SCOREBOARD_INGAME_HASITEM_NO: "&cNo"
SCOREBOARD_INGAME_LOOTCHEST_NOT_OPENED: "&cNot opened"
SCOREBOARD_INGAME_LOOTCHEST_OPENED: "&aOpened"
SCOREBOARD_INGAME_MOB_NOT_KILLED: "&cNot killed"
SCOREBOARD_INGAME_MOB_KILLED: "&aKilled"
SCOREBOARD_INGAME_NPCINTERACT_CLICK: "&aClick"
SCOREBOARD_INGAME_NPCINTERACT_LEFTCLICK: "&aLeft Click"
SCOREBOARD_INGAME_NPCINTERACT_RIGHTCLICK: "&aRight Click"
SCOREBOARD_INGAME_NPCINTERACT_YES: "&aYes"
SCOREBOARD_INGAME_NPCINTERACT_NO: "&cNo"
SCOREBOARD_INGAME_PLAYERPICKUP_YES: "&aYes"
SCOREBOARD_INGAME_PLAYERPICKUP_NO: "&cNo"


#
# Timer
#
TIMER_DAY: "d"
TIMER_HOUR: "h"
TIMER_MIN: "m"
TIMER_SEC: "s"


#
# GUI
#
GUI_INVALID_NAME: "Invalid name"

```
{% endcode %}
