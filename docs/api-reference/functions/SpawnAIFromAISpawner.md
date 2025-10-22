# SpawnAIFromAISpawner

Spawns one AI soldier from a specific AI Spawner. This function supports multiple overloads, allowing you to customize the spawned AI with different parameters such as soldier class, custom name, and team assignment.

## Syntax

```typescript
export function SpawnAIFromAISpawner(spawner: Spawner): void;
export function SpawnAIFromAISpawner(spawner: Spawner, classToSpawn: SoldierClass): void;
export function SpawnAIFromAISpawner(spawner: Spawner, name: Message): void;
export function SpawnAIFromAISpawner(spawner: Spawner, team: Team): void;
export function SpawnAIFromAISpawner(spawner: Spawner, classToSpawn: SoldierClass, name: Message): void;
export function SpawnAIFromAISpawner(spawner: Spawner, classToSpawn: SoldierClass, team: Team): void;
export function SpawnAIFromAISpawner(spawner: Spawner, name: Message, team: Team): void;
export function SpawnAIFromAISpawner(spawner: Spawner, classToSpawn: SoldierClass, name: Message, team: Team): void;
```

## Parameters

| Parameter    | Type               | Description                                                                      |
| ------------ | ------------------ | -------------------------------------------------------------------------------- |
| spawner      | `mod.Spawner`      | The AI Spawner object from which to spawn the AI soldier.                        |
| classToSpawn | `mod.SoldierClass` | (Optional) The soldier class for the spawned AI (e.g., Assault, Support, Medic). |
| name         | `mod.Message`      | (Optional) A custom message/name for the spawned AI soldier.                     |
| team         | `mod.Team`         | (Optional) The team to assign the spawned AI soldier to.                         |

## Example

```typescript
export async function OnGameModeStarted() {
  // Spawn AI with specific class and team
  mod.SpawnAIFromAISpawner(
    mod.GetSpawner(801), // Obj Id set in Godot
    mod.SoldierClass.Assault,
    mod.GetTeam(2)
  );
}
```

## See Also

- [`UnspawnAllAIsFromAISpawner`](UnspawnAllAIsFromAISpawner.md)
- [`AIEnableShooting`](AIEnableShooting.md)
- [`AIEnableTargeting`](AIEnableTargeting.md)
