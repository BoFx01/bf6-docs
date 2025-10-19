# SpawnObject

Spawns an object in the game.

## Syntax

```typescript
export function SpawnObject(
        prefabEnum:
            | RuntimeSpawn_Common
            | RuntimeSpawn_Abbasid
            | RuntimeSpawn_Aftermath
            | RuntimeSpawn_Battery
            | RuntimeSpawn_Capstone
            | RuntimeSpawn_Dumbo
            | RuntimeSpawn_FireStorm
            | RuntimeSpawn_Limestone
            | RuntimeSpawn_Outskirts
            | RuntimeSpawn_Tungsten,
        position: Vector,
        rotation: Vector
    ): Any;
```

## Parameters

| Parameter    | Type                 | Description                                    |
| ------------ | -------------------- | ---------------------------------------------- |
| `prefabEnum` | `mod.RuntimeSpawn_*` | The object to spawn from  `mod.RuntimeSpawn_*` |
| `position`   | `mod.Vector`         | Position on the map to place the object        |
| `rotation`   | `mod.Vector`         | Rotation vector                                |
| `scale`      | `mod.Vector`         | Scale vector                                   |

## Example

A simple example that spawns a world icon object.

```typescript
export async function OnGameModeStarted() {
  console.log("Game mode started");

  // Coordinates to place the object
  const pos = mod.CreateVector(341, 80, -202);

  // Spawn the icon
  const icon = mod.SpawnObject(mod.RuntimeSpawn_Common.WorldIcon, pos, mod.CreateVector(0, 0, 0));

  // Set the icon appearance
  mod.SetWorldIconImage(icon, mod.WorldIconImages.Skull);
  mod.SetWorldIconColor(icon, mod.CreateVector(1, 1, 1));
  mod.EnableWorldIconImage(icon, true);
}
```