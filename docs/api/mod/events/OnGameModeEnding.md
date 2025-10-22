# OnGameModeEnding

This function triggers when a game mode is ending. This is helpful for doing server cleanup, handling end-of-match logic, and setting up for the next match.

## Syntax

```typescript
export async function OnGameModeEnding(): void;
```

## Example

```typescript
export async function OnGameModeStarted() {
  console.log("Game mode started")
  const areaTrigger = mod.GetAreaTrigger(500);
  mod.EnableAreaTrigger(areaTrigger, true);
}

export async function OnPlayerEnterAreaTrigger(eventPlayer: mod.Player, eventAreaTrigger: mod.AreaTrigger) {
  if (mod.GetObjId(eventAreaTrigger) == 500) {
    console.log("Ending game mode");
    mod.EndGameMode(eventPlayer);
  }
}

// Display a message when the match has ended
export async function OnGameModeEnding() {
  console.log("Game has ended");
  const msg = mod.Message(mod.stringkeys.game_over);
  mod.DisplayNotificationMessage(msg);
}
```

## See Also

- [`EndGameMode`](../functions/EndGameMode.md)