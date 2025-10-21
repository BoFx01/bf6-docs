# OngoingTeam

This function executes continuously for the specified team throughout the game mode. It's useful for implementing team-based logic that needs to run repeatedly, such as monitoring team status, applying team-wide effects, or checking team conditions.

## Syntax

```typescript
export function OngoingTeam(eventTeam: mod.Team): void;
```

## Parameters

| Parameter | Type     | Description                                       |
| --------- | -------- | ------------------------------------------------- |
| eventTeam | mod.Team | The team for which the ongoing logic will execute |

## See Also

- [`OngoingPlayer`](OngoingPlayer.md)
- [`SetGameModeScore`](../functions/SetGameModeScore.md)
- [`SetHQTeam`](../functions/SetHQTeam.md)
