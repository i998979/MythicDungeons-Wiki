# GUIs

{% hint style="info" %}
**Reminder:** This page might not be updated regularly. You may check the changelog on the resource page or inside the downloaded jar.

Please let me know if you need additional placeholders.
{% endhint %}

## SignGUI and GUI Text (menu.yml)

Generally, all possible placeholders are already put inside. If you require more internal placeholders, please let me know.

Texts on SignGUI may not appear in all Minecraft versions. However, as long as you see the SignGUI appearing, even if it is empty, you can still input texts on the first line and it will still be detected and processed.

{% code title="menu.yml" lineNumbers="true" %}
```yaml
Menus:
  InputGUI:
    # Sign GUI when you search for rooms
    Search:
      - ""
      - "^^^^^^^^^^^^^^^^"
      - "Enter keyword"
      - "to search"
    # Sign GUI when you join a room with privacy PASSWORD
    Password:
      - ""
      - "^^^^^^^^^^^^^^^^"
      - "Please enter"
      - "room password"
    # Sign GUI when you are inside a room and wanted to invite someone
    Invite:
      - ""
      - "^^^^^^^^^^^^^^^^"
      - "Please enter"
      - "player name"
    # Sign GUI when you are creating a room and want to write some notes about the room
    Note:
      - ""
      - "^^^^^^^^^^^^^^^^"
      - "Please enter"
      - "the message"
  #
  #
  #
  # Only these options can be used when modifying the item
  #
  # Material: BEDROCK
  # Name: "Whatever you want, but only placeholders existed in the item below can be used"
  # Lores: "Whatever you want, but only placeholders existed in the item below can be used"
  # Amount: 64
  # Glow: true
  # Enchants:
  #   - ARROW_DAMAGE
  #   - ARROW_FIRE
  #   - ARROW_INFINITE
  #   - Whatever_you_want_existed_in
  #     https://hub.spigotmc.org/javadocs/spigot/org/bukkit/enchantments/Enchantment.html
  # ItemFlags:
  #   - HIDE_ATTRIBUTES
  #   - HIDE_DESTROYS
  #   - HIDE_DYE
  #   - Whatever_you_want_existed_in
  #     https://hub.spigotmc.org/javadocs/spigot/org/bukkit/inventory/ItemFlag.html
  # CustomModelData: 1
  # Unbreakable: true
  #
  #
  #
  Menu:
    Size: 54
    Name: "MythicDungeons rooms"
    Pane:
      Slot: "0 8 9 17 18 26 27 35 36 44 45 53"
      Material: WHITE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Head:
      Slot: "10 11 12 13 14 15 16 19 20 21 22 23 24 25 28 29 30 31 32 33 34 37 38 39 40 41 42 43"
      Material: PLAYER_HEAD
      Name: "&e%owner%"
      Lores:
        - "&7Id: %id%"
        - "&7Dungeon: %dungeon%"
        - "&7Members: %current%/%max%"
        - "&7Privacy: %privacy%"
        - "&7Note: %note%"
        - ""
        - "&7Left click to join"
        - "&7Right click to view"
    Previous:
      Slot: 46
      Material: ARROW
      Name: "&fPrevious page"
      Lores:
        - "&7%current%/%max%"
    Next:
      Slot: 52
      Material: ARROW
      Name: "&fNext page"
      Lores:
        - "&7%current%/%max%"
    Search:
      Slot: 48
      Material: OAK_SIGN
      Name: "&aSearch"
      Lores:
        # Nothing is filtered
        Empty:
          - "&7Find room by owner's name"
          - "&7room type, or room id."
          - ""
          - "&eClick to search!"
        # Filtered text included
        Filtered:
          - "&7Find room by owner's name"
          - "&7room type, or room id."
          - ""
          - "&7Filtered: &e%search%"
          - ""
          - "&bRight click to clear!"
          - "&eClick to edit filter!"
    Create:
      Slot: 49
      Material: END_PORTAL_FRAME
      Name: "&cCreate room"
      Lores:
        - "&7Have fun with your friends!"
    Return:
      Slot: 49
      Material: OAK_DOOR
      Name: "&aReturn to room"
      Lores:
        - "&7You are already inside a room,"
        - "&7click here to return."
    Sort:
      Slot: 50
      Material: HOPPER
      Name: "&aSort by"
      Lores:
        - "%c_none%> None"
        - "%c_name%> Owner name"
        - "%c_type%> Room type"
        - "%c_id%> Room id"
        - ""
        - "&eClick to change!"
      # Color code of selected sorting method
      Unselected: "&7"
      # Color code of unselected sorting method
      Selected: "&b"
  Confirm:
    Pane:
      Slot: "0 8 9 17 18 26 27 35 36 44"
      Material: WHITE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Confirm:
      Slot: "10 11 12 19 20 21 28 29 30"
      Material: EMERALD_BLOCK
      Name: "&aConfirm"
      Lores: [ ]
    Cancel:
      Slot: "14 15 16 23 24 25 32 33 34"
      Material: REDSTONE_BLOCK
      Name: "&cCancel"
      Lores: [ ]
    Message:
      Slot: 22
      Material: PLAYER_HEAD
      Name: "%name%"
      # You are not recommended adding lores here manually
      # because it should be added dynamically in other places
      # Lores: []
  Create:
    Size: 45
    Name: "Creating %dungeon% &rroom"
    Pane:
      Slot: "0 8 9 17 18 26 27 35 36 44"
      Material: WHITE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Min:
      Slot: 10
      Material: PLAYER_HEAD
      Name: "&cMinimum players"
      Lores:
        - "&7Left click to increase"
        - "&7Right click to decrease"
    Max:
      Slot: 12
      Material: PLAYER_HEAD
      Name: "&2Maximum players"
      Lores:
        - "&7Left click to increase"
        - "&7Right click to decrease"
    Public:
      Slot: 14
      Material: LIME_DYE
      Name: "&aPublic"
      Lores:
        - "&7Everyone can join!"
    Password:
      Slot: 15
      Material: MAGENTA_DYE
      Name: "&dPassword"
      Lores:
        - "&7Only invited players and"
        - "&7player with the password can join."
    Password_Set:
      Slot: 24
      Material: REDSTONE_LAMP
      Name: "&eSet password &7(Current: \"%password%\")"
      Lores:
        - "&7Change password to avoid"
        - "&7unexpected players joining in!"
    Private:
      Slot: 16
      Material: RED_DYE
      Name: "&cPrivate"
      Lores:
        - "&7Only invited players can join."
    AllInvite_Off:
      Slot: 30
      Material: GRAY_DYE
      Name: "&cAll invites"
      Lores:
        - "&7Only owner can invite"
        - "&7other players to the room"
    AllInvite_On:
      Slot: 30
      Material: LIME_DYE
      Name: "&aAll invites"
      Lores:
        - "&7Every member can invite"
        - "&7other players to the room"
    Note:
      Slot: 32
      Material: PAPER
      Name: "&aNote"
      Lores:
        - "&7Write some notes to tell"
        - "&7others your goal"
        - "&7(Current: %note%)"
    Cancel:
      Slot: 37
      Material: REDSTONE_BLOCK
      Name: "&cCancel"
      Lores: [ ]
    Create:
      Slot: 43
      Material: EMERALD_BLOCK
      Name: "&aCreate"
      Lores: [ ]
  Invite:
    Size: 54
    Name: "Viewing invitations..."
    Pane:
      Slot: "0 8 9 17 18 26 27 35 36 44 45 53"
      Material: WHITE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Invited:
      Slot: "0 8 9 17 18 26 27 35 36 44 45 53"
      Material: PLAYER_HEAD
      Name: "&e%name%"
      Lores:
        # Lore only show for room owner
        Owner:
          - "&cClick to remove invitation"
        # Lore only show for room members
        Member: [ ]
    Invite:
      Slot: 48
      Material: OAK_SIGN
      Name: "&aInvite"
      Lores:
        - "&7Invite online players"
        - "&7to the room and have fun!"
    Return:
      Slot: 49
      Material: ARROW
      Name: "&aReturn to room"
      Lores: [ ]
    Next:
      Slot: 52
      Material: ARROW
      Name: "&eNext page &7(%curr%/%max%)"
      Lores:
        - ""
        - "&bRight click to skip!"
    Previous:
      Slot: 46
      Material: ARROW
      Name: "&ePrevious page &7(%curr%/%max%)"
      Lores:
        - ""
        - "&bRight click to skip!"
  Ready:
    Size: 27
    Name: "Get ready for %dungeon%&r!"
    Pane:
      Slot: "1 2 3 4 5 6 7 19 20 21 22 23 24 25"
      Material: BLACK_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Pane2:
      Slot: "0 8 9 17 18 26"
      Material: WHITE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Three:
      Slot: "10 16"
      Material: YELLOW_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Two:
      Slot: "11 15"
      Material: ORANGE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    One:
      Slot: "12 14"
      Material: RED_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Cancel:
      Slot: "4 22"
      Material: REDSTONE_BLOCK
      Name: "&cCancel"
      Lores: [ ]
    Start:
      Slot: 13
      Material: DIAMOND_SWORD
      Name: "&ePrepare for %dungeon%&r&e!"
      ItemFlags:
        - HIDE_ATTRIBUTES
      Lores: [ ]
  Room:
    Size: 54
    Name: "%owner%'s %dungeon% &rroom"
    Pane:
      Slot: "0 8 9 17 18 26 27 35 36 44 45 53"
      Material: WHITE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Owner:
      Slot: 4
      Material: PLAYER_HEAD
      Name: "&eOwner: %owner%"
      Lores:
        # If the owner is online
        Online:
          - "&7Status: &aOnline"
        # If the owner is offline
        Offline:
          - "&7Status: &cOffline"
    Member:
      Material: PLAYER_HEAD
      Name: "&e%name%"
      Lores:
        # If the member is online
        Online:
          - "&7Status: &aOnline"
        # If the member is offline
        Offline:
          - "&7Status: &cOffline"
        # Only show to owner
        Owner:
          - "&7Left click to promote"
          - "&7Right click to remove"
    Previous:
      Slot: 43
      Material: ARROW
      Name: "&fPrevious page"
      Lores:
        - "&7%current%/%max%"
    Next:
      Slot: 37
      Material: ARROW
      Name: "&fNext page"
      Lores:
        - "&7%current%/%max%"
    Leave:
      Slot: 46
      Material: IRON_DOOR
      Name: "&cLeave"
      Lores: [ ]
    Info:
      Slot: 49
      Material: BOOK
      Name: "&aRoom information"
      Lores:
        # Info for privacy PUBLIC or PRIVATE
        Default:
          - "&7Id: %id%"
          - "&7Owner: %owner%"
          - "&7Dungeon: %dungeon%"
          - "&7Created: %created% ago"
          - "&7Privacy: %privacy%"
          - "&7Note: %note%"
        # Info for privacy PASSWORD
        Password:
          - "&7Id: %id%"
          - "&7Owner: %owner%"
          - "&7Dungeon: %dungeon%"
          - "&7Created: %created% ago"
          - "&7Privacy: %privacy%"
          - "&7Password: %password%"
          - "&7Note: %note%"
    Invite:
      Slot: 48
      Material: PLAYER_HEAD
      Name: "&aInvitation to players"
      Lores:
        # If all invite is on
        AllInvite_On:
          - "&7Invite your friends to the room"
          - "&7and challenge the dungeon with them!"
        # If all invite is off
        AllInvite_Off:
          - "&7Check the pending invitations"
          - "&7tell your friends to accept invitations!"
    Settings:
      Slot: 50
      Material: COMPARATOR
      Name: "&aSettings"
      Lores:
        - "&7Change min, max players"
        - "&7and privacy settings here."
    Start:
      Slot: 52
      Material: DIAMOND_SWORD
      Name: "&aStart"
      Enchants:
        - DAMAGE_ALL 1
      ItemFlags:
        - HIDE_ATTRIBUTES
      Lores:
        - "&7Challenge dungeon %dungeon% &r&7!"
    Leaving:
      Title: "Confirm leaving?"
      Name: "&e%owner%'s %dungeon% &r&eroom"
      Lores:
        - "&7Id: %id%"
        - "&7Owner: %owner%"
        - "&7Dungeon: %dungeon%"
    Promotion:
      Title: "Confirm promotion?"
      Name: "&ePromote %name% to owner"
      Lores:
        - "&7Id: %id%"
        - "&7Owner: %owner%"
        - "&7Dungeon: %dungeon%"
    Removal:
      Title: "Confirm removal?"
      Name: "&eRemove %name% from the room"
      Lores:
        - "&7Id: %id%"
        - "&7Owner: %owner%"
        - "&7Dungeon: %dungeon%"
  RoomInfo:
    Size: 54
    Name: "Viewing %owner%'s %dungeon% &rroom"
    Pane:
      Slot: "0 8 9 17 18 26 27 35 36 44 45 53"
      Material: WHITE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Owner:
      Slot: 4
      Material: PLAYER_HEAD
      Name: "&eOwner: %owner%"
      Lores:
        Online:
          - "&7Status: &aOnline"
        Offline:
          - "&7Status: &cOffline"
    Member:
      Slot: "10 11 12 13 14 15 16 19 20 21 22 23 24 25 28 29 30 31 32 33 34 37 38 39 40 41 42 43"
      Material: PLAYER_HEAD
      Name: "&e%name%"
      Lores:
        Online:
          - "&7Status: &aOnline"
        Offline:
          - "&7Status: &cOffline"
        Owner:
          - "&7Left click to promote"
          - "&7Right click to remove"
    Previous:
      Slot: 43
      Material: ARROW
      Name: "&fPrevious page"
      Lores:
        - "&7%current%/%max%"
    Next:
      Slot: 37
      Material: ARROW
      Name: "&fNext page"
      Lores:
        - "&7%current%/%max%"
    Return:
      Slot: 46
      Material: IRON_DOOR
      Name: "&cReturn to menu"
      Lores: [ ]
    Info:
      Slot: 49
      Material: BOOK
      Name: "&aRoom information"
      Lores:
        - "&7Id: %id%"
        - "&7Owner: %owner%"
        - "&7Dungeon: %dungeon%"
        - "&7Created: %created% ago"
        - "&7Note: %note%"
  Settings:
    Size: 45
    Name: "Modifying %dungeon% &rroom..."
    Pane:
      Slot: "0 8 9 17 18 26 27 35 36 44"
      Material: WHITE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Min:
      Slot: 10
      Material: PLAYER_HEAD
      Name: "&cMinimum players"
      Lores:
        - "&7Left click to increase"
        - "&7Right click to decrease"
    Max:
      Slot: 12
      Material: PLAYER_HEAD
      Name: "&2Maximum players"
      Lores:
        - "&7Left click to increase"
        - "&7Right click to decrease"
    Public:
      Slot: 14
      Material: LIME_DYE
      Name: "&aPublic"
      Lores:
        - "&7Everyone can join!"
    Password:
      Slot: 15
      Material: MAGENTA_DYE
      Name: "&dPassword"
      Lores:
        - "&7Only invited players and"
        - "&7player with the password can join."
    Password_Set:
      Slot: 24
      Material: REDSTONE_LAMP
      Name: "&eSet password &7(Current: \"%password%\")"
      Lores:
        - "&7Change password to avoid"
        - "&7unexpected players joining in!"
    Private:
      Slot: 16
      Material: RED_DYE
      Name: "&cPrivate"
      Lores:
        - "&7Only invited players can join."
    AllInvite_Off:
      Slot: 30
      Material: GRAY_DYE
      Name: "&cAll invites"
      Lores:
        - "&7Only owner can invite"
        - "&7other players to the room"
    AllInvite_On:
      Slot: 30
      Material: LIME_DYE
      Name: "&aAll invites"
      Lores:
        - "&7Every member can invite"
        - "&7other players to the room"
    Return:
      Slot: 40
      Material: ARROW
      Name: "&aReturn to room"
      Lores: [ ]
    Note:
      Slot: 32
      Material: PAPER
      Name: "&aNote"
      Lores:
        - "&7Write some notes to tell"
        - "&7others your goal"
        - "&7(Current: %note%)"
  Type:
    Size: 54
    Name: "Please select a dungeon type..."
    Pane:
      Slot: "0 8 9 17 18 26 27 35 36 44 45 53"
      Material: WHITE_STAINED_GLASS_PANE
      Name: " "
      Lores: [ ]
    Return:
      Slot: 49
      Material: ARROW
      Name: "&aReturn to menu"
      Lores: [ ]
    Info:
      Slot: 50
      Material: BOOK
      Name: "&aType information"
      Lores:
        - "&7Select the type of dungeon"
        - "&7you want to challenge by"
        - "&7clicking the icons above."
    Next:
      Slot: 52
      Material: ARROW
      Name: "&eNext page &7(%curr%/%max%)"
      Lores:
        - ""
        - "&bRight click to skip!"
    Previous:
      Slot: 46
      Material: ARROW
      Name: "&ePrevious page &7(%curr%/%max%)"
      Lores:
        - ""
        - "&bRight click to skip!"
```
{% endcode %}
