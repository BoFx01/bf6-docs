# OnPlayerLeaveGame

This function triggers when any player leaves the game. Note that this callback receives a player number rather than a Player object, as the player has already disconnected.

## Syntax

```typescript
export function OnPlayerLeaveGame(eventNumber: number): void;
```

## Parameters

| Parameter     | Type     | Description                                   |
| ------------- | -------- | --------------------------------------------- |
| `eventNumber` | `number` | The number/ID of the player who left the game |

## Example

=== "Script.ts"
    ```typescript
    export function OnPlayerLeaveGame(eventNumber: number) {
      console.log(`Player ${eventNumber} has left the game`);
      
      // Clean up any player-specific data
      // Note: Player object is no longer available, only the player number
      
      // Display a message to remaining players
      const leaveMsg = mod.Message(mod.stringkeys.goodbye);
      mod.DisplayNotificationMessage(leaveMsg);
    }
    ```
=== "Strings.json"
    ```json
    {
      "goodbye": "A player disconnected."
    }
    ```

## See Also

- [`OnPlayerJoinGame`](./OnPlayerJoinGame.md)