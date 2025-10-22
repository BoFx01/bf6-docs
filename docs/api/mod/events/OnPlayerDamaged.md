# OnPlayerDamaged

This function triggers when a player takes damage from any source. This is useful for tracking damage events, implementing custom damage logic, or creating damage-based game mechanics. This function is called repeatedly if a player is down and bleeding out.

## Syntax

```typescript
export function OnPlayerDamaged(
    eventPlayer: mod.Player,
    eventOtherPlayer: mod.Player,
    eventDamageType: mod.DamageType,
    eventWeaponUnlock: mod.WeaponUnlock
): void;
```

## Parameters

| Parameter           | Type               | Description                        |
| ------------------- | ------------------ | ---------------------------------- |
| `eventPlayer`       | `mod.Player`       | The player who took damage         |
| `eventOtherPlayer`  | `mod.Player`       | The player who dealt the damage    |
| `eventDamageType`   | `mod.DamageType`   | The type of damage dealt           |
| `eventWeaponUnlock` | `mod.WeaponUnlock` | The weapon used to deal the damage |

## Example

=== "Script.ts"
    ```typescript
    export function OnPlayerDamaged(
        eventPlayer: mod.Player,
        eventOtherPlayer: mod.Player,
        eventDamageType: mod.DamageType,
        eventWeaponUnlock: mod.WeaponUnlock
    ) {
        
      const msg = mod.Message(mod.stringkeys.damaged, eventPlayer);
      mod.DisplayNotificationMessage(msg);
    }
    ```
=== "Strings.json"
    ```json
    {
      "damaged": "{} is taking damage!"
    }
    ```

![Screen capture of player taking damage](../../../img/OnPlayerDamaged_example.gif)

## See Also

- [`OnPlayerDied`](./OnPlayerDied.md)
- [`OnMandown`](./OnMandown.md)
- [`DealDamage`](../functions/DealDamage.md)
- [`Heal`](../functions/Heal.md)
