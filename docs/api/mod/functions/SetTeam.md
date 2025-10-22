# SetTeam

This function changes the team assignment of a specified player. This is useful for dynamically balancing teams, creating custom team-switching mechanics, or implementing game modes that require players to change teams during gameplay.

## Syntax

```typescript
export function SetTeam(player: Player, team: Team): void;
```

## Parameters

| Parameter | Type         | Description                           |
| --------- | ------------ | ------------------------------------- |
| player    | `mod.Player` | The player whose team will be changed |
| team      | `mod.Team`   | The team to assign the player to      |

## Example

```typescript
export async function OnPlayerJoinGame(eventPlayer: mod.Player) {
  console.log("Player joined the game");
  mod.SetTeam(eventPlayer, mod.GetTeam(2));
}
```

## See Also

- [`GetTeam`](GetTeam.md)
- [`GetSquad`](GetSquad.md)
- [`SetHQTeam`](SetHQTeam.md)
