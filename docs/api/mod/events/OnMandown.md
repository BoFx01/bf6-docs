# OnMandown

This function triggers when a player is forced into the mandown state (incapacitated but not yet dead). This is useful for implementing revive mechanics, tracking incapacitations, and creating special gameplay events. Both this and `OnPlayerDied` is called at the same time when the player is initially downed.

## Syntax

```typescript
export function OnMandown(eventPlayer: mod.Player, eventOtherPlayer: mod.Player): void;
```

## Parameters

| Parameter          | Type         | Description                                            |
| ------------------ | ------------ | ------------------------------------------------------ |
| `eventPlayer`      | `mod.Player` | The player who entered the mandown state               |
| `eventOtherPlayer` | `mod.Player` | The player who caused the eventPlayer to enter mandown |

## Example

=== "Script.ts"
    ```typescript
    export function OnMandown(eventPlayer: mod.Player, eventOtherPlayer: mod.Player) {
        const msg = mod.Message(mod.stringkeys.down, eventPlayer);
        mod.DisplayNotificationMessage(msg);
    }
    ```
=== "Strings.json"
    ```json
    {
      "down": "{} is down and needs assistance!"
    }
    ```

![Screen capture of player being downed](../../../img/OnMandown_example.gif)

## See Also

- [`OnPlayerDied`](./OnPlayerDied.md)
- [`OnPlayerDamaged`](./OnPlayerDamaged.md)
- [`ForceRevive`](../functions/ForceRevive.md)
