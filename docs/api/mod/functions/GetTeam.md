# GetTeam

Returns the team value of the specified player or the corresponding team of the provided number. This function allows you to retrieve team information either by passing a player object or by using a team ID number.

## Syntax

```typescript
export function GetTeam(player: Player): Team;
export function GetTeam(teamId: number): Team;
```

## Parameters

| Parameter | Type         | Description                                        |
| --------- | ------------ | -------------------------------------------------- |
| `player`  | `mod.Player` | The player object to retrieve the team from        |
| `teamId`  | `number`     | The team ID number to retrieve the team object for |

## Return Values

| Type       | Description                                            |
| ---------- | ------------------------------------------------------ |
| `mod.Team` | The team object corresponding to the player or team ID |

## Example

```typescript
// Get team from a player
export async function OnPlayerJoinGame(eventPlayer: mod.Player) {
  const playerTeam = mod.GetTeam(eventPlayer);
  console.log("Player joined team:", playerTeam);
}

// Get team from a team ID
export async function OnPlayerJoinGame(eventPlayer: mod.Player) {
  console.log("Player joined the game");
  const teamId = mod.GetTeam(2)
  mod.SetTeam(eventPlayer, teamId);
}
```

## See Also

- [`SetTeam`](SetTeam.md)
