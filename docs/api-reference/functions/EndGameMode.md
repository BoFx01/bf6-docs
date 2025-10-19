# EndGameMode

Ends the current game with a winning team or player.

## Syntax
```typescript
export function EndGameMode(player: Player): void; // Winning player
export function EndGameMode(team: Team): void; // Winning team
export function EndGameMode(0): void; // Draw - no winner
```

## Parameters

| Parameter                 | Type            | Description                       |
| ------------------------- | --------------- | --------------------------------- |
| `player` or `team` or `0` | `Player\|Team\` | Team or player that is the winner |

## Example

```typescript
export async function OnGameModeStarted() {
  console.log("Game mode started")
  const areaTrigger = mod.GetAreaTrigger(500);
  mod.EnableAreaTrigger(areaTrigger, true);
}

// End the game. The player taht entered the area trigger is the winner.
export async function OnPlayerEnterAreaTrigger(eventPlayer: mod.Player, eventAreaTrigger: mod.AreaTrigger) {
  if (mod.GetObjId(eventAreaTrigger) == 500) {
    console.log("Ending game mode");
    mod.EndGameMode(eventPlayer);
  }
}

export async function OnGameModeEnding() {
  console.log("Game has ended");
  const msg = mod.Message(mod.stringkeys.game_over);
  mod.DisplayNotificationMessage(msg);
}
```

## See Also

- [`OnGameModeEnding`](../event-handlers/OnGameModeEnding.md)
