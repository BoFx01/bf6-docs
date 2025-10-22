# OnGameModeStarted

This function triggers at the start of the gamemode. This can be used as the entry point to initialize the game.

## Syntax

```typescript
export function OnGameModeStarted(): void;
```

## Example

```typescript
// Display a message to all players every minute
export async function OnGameModeStarted() {
  while (true) {
    mod.DisplayNotificationMessage(mod.Message(mod.stringkeys.s1));
    await mod.Wait(60);
  }
}
```