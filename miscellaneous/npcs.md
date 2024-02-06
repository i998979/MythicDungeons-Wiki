# NPCs

Citizens is used to create NPC-related features. Please make sure you have [Citizens](https://www.spigotmc.org/resources/citizens.13811/) installed on your server.

Citizens NPC is saved inside `MythicDungeons/saves.yml`. Please create one if you want to use NPC-related features.

MythicDungeons does not provide any method to create/copy NPC. However, you can create an NPC using Citizens command, save it using `/Citizens save`, open `Citizens/saves.yml`, copy the NPC into `MythicDungeons/saves.yml`, and replace world and coordinates using [Placeholders](placeholders.md). The plugin will parse placeholders inside before the dungeon is started.

{% code title="saves.yml" lineNumbers="true" %}
```yaml
# Citizens NPC Storage

last-created-npc-id: 1
npc:
  '1':
    metadata:
      cached-skin-uuid: 991d961c-b6b4-4d49-88e6-01788cf445dc
      cached-skin-uuid-name: i9_14900k
    name: i9_14900K
    uuid: ebda02e9-48eb-4f6e-82d7-2de8fd5a8f95
    traits:
      type: PLAYER
      owner:
        uuid: 991d961c-b6b4-4d49-88e6-01788cf445dc
      skintrait:
        fetchDefaultSkin: true
        signature: Ejyo9ry8TIXAuj0QCS920+xOXlWpvbF1vJ9SLvPJYYmvGr5/MUamKe2NsXMxdELCty+TvhQfucO9BmIbTCCOmmIjrhgK1UpIsryVxpYI4LsTI8IZN7UZ8cYYFPM3wcK58NBz5SRM7l04+B3cVLiJA2jzYjQEyWb/NF+D8dV9W7GiG0upuTyx6s5jW7+o0Z5ortegDPE+howhFlbQyj6YPzWZp/2rAJNc+2zS8G4j5HIc5p4nHNwxUAjWLJYzFlM0Elg9Tii7JHTSw7eIi/DzpsMVeOxjQTZ88UPnlp6dNm5fRm8InnK9Vdb/0QKQiBdiIU5gVP52FoRSk7A8oY70ZHKbBIVaplk9yG/+ccbEyO29DhVZdstA5vxZMJ7xhmMsqMByQsur5p4/Yx9swhixv44yWK0c491uIZ2dSMjEjfsIoqYUs4L/HLIoWW3fCk/DKFBU6slbsCBBYcmCSxZVk+Rut42pOUozp1Ns/AMXHauBlPCb57uoVlUqj1r2QC3WZpq2Sp1wQ36njPchHyJEryfiQyrBfXkFJCj+w6JXMQb+8Sk0+u+9zrcNjTj3QyPpIwUhI633S2pbrMqd0TVXbVR/MiHblKDq4qKDiA7k3MPiMoaeLpNZ4krxKenkitjI5AOrdbZMh9zoYEtcgCDvXtR+pDkjk0Z2iBCXOpyhT/o=
        textureRaw: ewogICJ0aW1lc3RhbXAiIDogMTcwNjYxNTYxNTU5MywKICAicHJvZmlsZUlkIiA6ICI5OTFkOTYxY2I2YjQ0ZDQ5ODhlNjAxNzg4Y2Y0NDVkYyIsCiAgInByb2ZpbGVOYW1lIiA6ICJpOV8xNDkwMEsiLAogICJzaWduYXR1cmVSZXF1aXJlZCIgOiB0cnVlLAogICJ0ZXh0dXJlcyIgOiB7CiAgICAiU0tJTiIgOiB7CiAgICAgICJ1cmwiIDogImh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMTA4M2Q4MjM2NWQ1MTEyM2EyNjMyNzcxM2M2ZjllNmU1ZTZjMWU0ZGJkYmIwMzg0OWYxZjZlOWNlYWFiZTEwYSIKICAgIH0sCiAgICAiQ0FQRSIgOiB7CiAgICAgICJ1cmwiIDogImh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMjM0MGMwZTAzZGQyNGExMWIxNWE4YjMzYzJhN2U5ZTMyYWJiMjA1MWIyNDgxZDBiYTdkZWZkNjM1Y2E3YTkzMyIKICAgIH0KICB9Cn0=
        updateSkins: false
      location:
        bodyYaw: -0.52426267
        world: '%mythicdungeons_dungeon_origin_world%'
        x: '%mythicdungeons_dungeon_origin_x%'
        y: '%mythicdungeons_dungeon_origin_y%'
        z: '%mythicdungeons_dungeon_origin_z%'
        yaw: '-0.5243'
        pitch: '-5.7066'
    traitnames: inventory,scoreboardtrait,type,spawned,owner,mounttrait,skintrait,location
    navigator:
      speedmodifier: '1.0'
      avoidwater: false
      usedefaultstuckaction: false

```
{% endcode %}

## Explanation

Everything is similar to Citizens `saves.yml`. However, the location is replaced with PlaceholderAPI's placeholder, and this NPC will be spawned at the origin of the dungeon.

```yaml
 location:
   bodyYaw: -0.52426267
   world: '%mythicdungeons_dungeon_origin_world%'
   x: '%mythicdungeons_dungeon_origin_x%'
   y: '%mythicdungeons_dungeon_origin_y%'
   z: '%mythicdungeons_dungeon_origin_z%'
   yaw: '-0.5243'
   pitch: '-5.7066'
```
