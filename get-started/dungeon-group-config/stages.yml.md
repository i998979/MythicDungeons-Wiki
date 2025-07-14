# stages.yml

## Stages (Simplified)

This dungeon requires killing 1 `SkeletalKnight` within `60` seconds to finish.

```yaml
# Main flow of the dungeon
Stages:
  # ID of the stage, must be unique
  '0':
    Options:
      # True if this is the first stage of the dungeon, only 1 can exist
      Initial: true
      # True if this is the last stage of the dungeon, more than 1 can exist
      End: true
    # A list of actions will do when this stage starts
    Actions:
      - MythicMob{type=SkeletalKnight;at=LOCATION;world=dungeon;x=120.5;y=6.0;z=259.5;yaw=0.0;pitch=0.0}
    # A list of objectives needs to be fulfilled to complete this stage
    Objectives:
      - MythicMob{type=SkeletalKnight;amount=1}
    # Objective display of the stage
    Displays:
      # Scoreboard display of the stage
      Scoreboard:
        # Interval of the title changes
        Interval: 10
        # Title of the scoreboard display
        # If no title lines are specified, the next stage with objective lines specified
        # will inherit previous active titles
        Titles:
          - "&6&lMythicDungeons"
          - "&eMythicDungeons"
        # Interval of the objective line scrolls if objective lines
        # does not fit pre-defined spaces
        ScrollInterval: 20
        # Lines of the scoreboard display, use %objectives% to show objective lines
        # If no lines are specified, the next stage with objective lines specified
        # will inherit previous active lines
        Lines:
          - "&0"
          - "&eDungeon||&f%dungeon%"
          - "&eTime left||&f%expire%"
          - "&1"
          - "&2%objective%"
          - "&3%objective%"
          - "&4%objective%"
          - "&5%objective%"
        # Objective lines of the stage, follows the order where Objectives are defined
        Objectives:
          - '&fSlain %MythicMob_1_mobamtkilled%/%MythicMob_1_mobamtmax%x %MythicMob_1_mobamtkill%'
    # A list of actions will do when this stage is completed
    Completions: [ ]
    # A list of actions will do when the dungeon fails during this stage
    FailActions: [ ]
    # A list of stages that will start when this stage is completed
    Branches: [ ]
```

## Stages (Full)

If you are familiar with the configuration, here is a full configuration.

```yaml
# Main flow of the dungeon
Stages:
  # ID of the stage, must be unique
  '0':
    Options:
      # True if this is the first stage of the dungeon, only 1 can exist
      Initial: true
    # A list of actions will do when this stage starts
    Actions:
      - MythicSpawner{type=rat1;world=dungeon;x=116.0;y=5.0;z=255.0;yaw=0.0;pitch=0.0;settings=rat1.yml}
      - MythicSpawner{type=rat1;world=dungeon;x=116.0;y=5.0;z=252.0;yaw=0.0;pitch=0.0;settings=rat1.yml}
      - MythicSpawner{type=rat2;world=dungeon;x=124.0;y=5.0;z=252.0;yaw=0.0;pitch=0.0;settings=rat2.yml}
    # A list of objectives needs to be fulfilled to complete this stage
    Objectives:
      - MythicMob{type=rat1;amount=3}
      - Checkpoint{id=1}
    Displays:
      Scoreboard:
        Interval: 10
        Titles:
          - "&6&lMythicDungeons"
          - "&eMythicDungeons"
        ScrollInterval: 20
        Lines:
          - "&0"
          - "&eDungeon||&f%dungeon%"
          - "&eTime left||&f%expire%"
          - "&1"
          - "&2%objective%"
          - "&3%objective%"
          - "&4%objective%"
          - "&5%objective%"
        Objectives:
          - '&eSlain %MythicMob_1_mobamtkill%||(%MythicMob_1_mobamtkilled%/%MythicMob_1_mobamtmax%)'
          - ''
          - '&fDiscover the secret of %Checkpoint_2_cp%||&f%Checkpoint_2_cpreached%'
          - ''
      BossBar:
        Interval: 20
        Lines:
          - '&fSlain %MythicMob_1_mobamtkilled%/%MythicMob_1_mobamtmax%x %MythicMob_1_mobamtkill%'
          - ''
          - "{progress=1.0;color=PURPLE;style=SEGMENTED_20;message='&fDiscover the secret of %Checkpoint_2_cp%: %Checkpoint_2_cpreached%'}"
          - "{progress=%BlockBreak_3_progress%;message='&fBreak %BlockBreak_3_broke%/%BlockBreak_3_amount% %BlockBreak_3_block%'}"
          # - "{progress=index;message='&fBreak %BlockBreak_3_broke%/%BlockBreak_3_amount% %BlockBreak_3_block%'}"
      ActionBar:
        Interval: 20
        Lines:
          - '&fSlain %MythicMob_1_mobamtkilled%/%MythicMob_1_mobamtmax%x %MythicMob_1_mobamtkill%'
          - ''
          - '&fDiscover the secret of %Checkpoint_2_cp%: %Checkpoint_2_cpreached%'
    # A list of actions will do when this stage is completed
    Completions: [ ]
    # A list of actions will do when the dungeon fails during this stage
    FailActions: [ ]
    # A list of stages that will start when this stage is completed
    Branches:
      - Branch{id=1}
      # - Branch{id=2}
  '1':
    Options:
      # How long(in ticks) before this stage starts
      Delay: 0
    Actions:
      - MythicMob{type=rat3;at=LOCATION;world=dungeon;x=120.5;y=5.0;z=259.5;yaw=180.0;pitch=0.0}
    Objectives:
      - MythicMob{type=rat2;amount=2}
    Displays:
      Scoreboard:
        Interval: 10
        Titles:
          - "&2&lMythicDungeons"
          - "&aMythicDungeons"
        ScrollInterval: 20
        Lines:
          - "&0"
          - "&eDungeon||&f%dungeon%"
          - "&eTime left||&f%expire%"
          - "&1"
          - "&2%objective%"
          - "&3%objective%"
          - "&4%objective%"
          - "&5%objective%"
        Objectives:
          - '&eSlain %MythicMob_1_mobamtkill%||(%MythicMob_1_mobamtkilled%/%MythicMob_1_mobamtmax%)'
          - ''
      BossBar:
        Interval: 20
        Lines:
          - '&eKill %MythicMob_1_mobamtkilled%/%MythicMob_1_mobamtmax%x %MythicMob_1_mobamtkill%'
          - ''
      ActionBar:
        Interval: 20
        Lines:
          - '&eKill %MythicMob_1_mobamtkilled%/%MythicMob_1_mobamtmax%x %MythicMob_1_mobamtkill%'
          - ''
    Completions: [ ]
    FailActions: [ ]
    Branches:
      - Branch{id=2}
  '2':
    Options:
      # True if this is the last stage of the dungeon, more than 1 can exist
      End: true
    Actions:
      - MythicMob{type=rat4;at=NEARBY;radius=10.0}
    Objectives:
      - MythicMob{type=rat4}
    Displays:
      Scoreboard:
        Interval: 10
        Titles:
          - "&b&lMythicDungeons"
          - "&1MythicDungeons"
        ScrollInterval: 20
        Lines:
          - "&0"
          - "&eDungeon||&f%dungeon%"
          - "&eTime left||&f%expire%"
          - "&1"
          - "&2%objective%"
          - "&3%objective%"
          - "&4%objective%"
          - "&5%objective%"
        Objectives:
          - '&cKill %MythicMob_1_mobkill%'
          - ''
      BossBar:
        Interval: 20
        Lines:
          - '&cKill %MythicMob_1_mobkill%'
          - ''
      ActionBar:
        Interval: 20
        Lines:
          - '&cKill %MythicMob_1_mobkill%'
          - ''
    Completions:
      - Message{text='&d&lIMPRESSIVE, you have completed the challenge, you may now leave.'}
    FailActions: [ ]
    Branches: [ ]
```
