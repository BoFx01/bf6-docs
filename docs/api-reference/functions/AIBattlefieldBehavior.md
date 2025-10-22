# AIBattlefieldBehavior

Sets a player to act independently. They will attempt to complete objectives, fire on enemy players, and engage in autonomous battlefield behavior. This function only works for AI players.

## Syntax

```typescript
export function AIBattlefieldBehavior(player: Player): void;
```

## Parameters

| Parameter | Type         | Description                                        |
| --------- | ------------ | -------------------------------------------------- |
| player    | `mod.Player` | The AI player to set to battlefield behavior mode. |

## Example

```typescript
// Spawn AI soldiers when the game mode starts
export async function OnGameModeStarted() {
  // Spawn AI with specific class and team
  mod.SpawnAIFromAISpawner(
    mod.GetSpawner(801), // Obj Id set in Godot
    mod.SoldierClass.Assault,
    mod.GetTeam(2)
  );
}

// Set AI to battlefield behavior when they deploy
export function OnPlayerDeployed(eventPlayer: mod.Player) {
  const isAiSoldier = mod.GetSoldierState(eventPlayer, mod.SoldierStateBool.IsAISoldier);
  if (isAiSoldier) {
    // AI will now autonomously complete objectives and engage enemies
    mod.AIBattlefieldBehavior(eventPlayer);
  }
}
```

## See Also

- [`SpawnAIFromAISpawner`](./SpawnAIFromAISpawner.md)
- [`OnPlayerDeployed`](./OnPlayerDeployed.md)
- [`OnGameModeStarted`](./OnGameModeStarted.md)
- [`GetSoldierState`](./GetSoldierState.md)
