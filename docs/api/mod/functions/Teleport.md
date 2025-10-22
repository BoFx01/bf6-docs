# Teleport

Teleports a player or vehicle to a specified position in the world, facing a particular direction. This function is useful for moving entities to custom spawn points, creating teleport zones, or repositioning players/vehicles during gameplay.

## Syntax

```typescript
export function Teleport(player: Player, destination: Vector, orientation: number): void;
export function Teleport(vehicle: Vehicle, destination: Vector, orientation: number): void;
```

## Parameters

| Parameter            | Type                         | Description                                                        |
| -------------------- | ---------------------------- | ------------------------------------------------------------------ |
| `player` / `vehicle` | `mod.Player` / `mod.Vehicle` | The player or vehicle to teleport                                  |
| `destination`        | `mod.Vector`                 | The target position in world space coordinates                     |
| `orientation`        | `number`                     | The direction the entity should face after teleporting, in radians |

## Example

```typescript
type Vector3 = { x: number; y: number; z: number };

const spawnPoints: Record<number, Vector3> = {
  1: { x: 260, y: 88, z: -214 }
};

function sendPlayerToSpawnpoint(player: mod.Player, id: number) {
  const sp = spawnPoints[id];
  const pos = mod.CreateVector(sp.x, sp.y, sp.z);
  mod.Teleport(player, pos, 0);
}

export async function OnPlayerDeployed(eventPlayer: mod.Player) {
  sendPlayerToSpawnpoint(eventPlayer, 1);
}
```

## See Also

- [`CreateVector`](../functions/CreateVector.md)
- [`DeployPlayer`](../functions/DeployPlayer.md)
- [`SpawnPlayerFromSpawnPoint`](../functions/SpawnPlayerFromSpawnPoint.md)
- [`WorldPositionOf`](../functions/WorldPositionOf.md)
- [`OnPlayerDeployed`](../events/OnPlayerDeployed.md)
