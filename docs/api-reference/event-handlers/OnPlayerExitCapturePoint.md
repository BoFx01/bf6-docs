# OnPlayerExitCapturePoint

This function triggers when a player exits a CapturePoint capturing area. This is useful for implementing game logic such as stopping capture timers, updating UI notifications, or handling point contestation rules.

## Syntax

```typescript
export function OnPlayerExitCapturePoint(eventPlayer: mod.Player, eventCapturePoint: mod.CapturePoint): void;
```

## Parameters

| Parameter           | Type               | Description                                  |
| ------------------- | ------------------ | -------------------------------------------- |
| `eventPlayer`       | `mod.Player`       | The player who exited the capture point area |
| `eventCapturePoint` | `mod.CapturePoint` | The capture point that was exited            |

## Example

=== "Script.ts"
    ```typescript
    export function OnPlayerEnterCapturePoint(eventPlayer: mod.Player, eventCapturePoint: mod.CapturePoint) {
      // Display notification to all players
      const msg = mod.Message(mod.stringkeys.capture_enter, eventPlayer);
      mod.DisplayNotificationMessage(msg);
    }

    export function OnPlayerExitCapturePoint(eventPlayer: mod.Player, eventCapturePoint: mod.CapturePoint) {
      // Display notification to all players
      const msg = mod.Message(mod.stringkeys.capture_exit, eventPlayer);
      mod.DisplayNotificationMessage(msg);
    }
    ```
=== "Strings.json"
    ```json
    {
      "capture_enter": "{} entered the capture point.",
      "capture_exit": "{} exited the capture point."
    }
    ```

![Screen recording of player entering and exiting a capture point](../../img/OnPlayerCapture_example.gif)

## See Also

- [`OnPlayerEnterCapturePoint`](./OnPlayerEnterCapturePoint.md)
- [`OnPlayerExitAreaTrigger`](./OnPlayerExitAreaTrigger.md)
- [`CapturePoint`](../types/CapturePoint.md)
