# OnPlayerEnterAreaTrigger

Triggers when a player enters an [`AreaTrigger`](../types/AreaTrigger.md).

## Syntax

```typescript
export function OnPlayerEnterAreaTrigger(eventPlayer: mod.Player, eventAreaTrigger: mod.AreaTrigger): void;
```

## Parameters

| Parameter     | Type                                     | Description                             |
| ------------- | ---------------------------------------- | --------------------------------------- |
| `eventPlayer`      | [`Player`](../types/Player.md)           | The player who entered the area trigger |
| `eventAreaTrigger` | [`AreaTrigger`](../types/AreaTrigger.md) | The area trigger that was entered       |

## Example

**script.ts**
```typescript
// Enable the area trigger when the game starts
export async function OnGameModeStarted() {
  console.log("Game mode started")
  const areaTrigger = mod.GetAreaTrigger(500);
  mod.EnableAreaTrigger(areaTrigger, true);
}

// Publish a message
export async function OnPlayerEnterAreaTrigger(eventPlayer: mod.Player, eventAreaTrigger: mod.AreaTrigger) {
  const msg = mod.Message(mod.stringkeys.s0);
  mod.DisplayNotificationMessage(msg);
}
```

**strings.json**
```json
{
  "s0": "A player entered an area trigger"
}
```