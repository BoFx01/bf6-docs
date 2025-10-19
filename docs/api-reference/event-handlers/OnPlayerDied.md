# OnPlayerDied

This function triggers whenever a player dies. This is essential for implementing respawn logic, tracking kills and deaths, and handling post-death game mechanics. This function is called when a player is initially downed and is waiting to be revived.

## Syntax

```typescript
export function OnPlayerDied(
    eventPlayer: mod.Player,
    eventOtherPlayer: mod.Player,
    eventDeathType: mod.DeathType,
    eventWeaponUnlock: mod.WeaponUnlock
): void;
```

## Parameters

| Parameter           | Type               | Description                           |
| ------------------- | ------------------ | ------------------------------------- |
| `eventPlayer`       | ` mod.Player`      | The player who died                   |
| `eventOtherPlayer`  | `mod.Player`       | The player who killed the eventPlayer |
| `eventDeathType`    | `mod.DeathType`    | The type of death that occurred       |
| `eventWeaponUnlock` | `mod.WeaponUnlock` | The weapon used to kill the player    |

## Example

=== "Script.ts"
    ```typescript
    export function OnPlayerDied(
        eventPlayer: mod.Player,
        eventOtherPlayer: mod.Player,
        eventDeathType: mod.DeathType,
        eventWeaponUnlock: mod.WeaponUnlock
    ) {
        // Display a kill notification
        const msg = mod.Message(mod.stringkeys.died, eventOtherPlayer, eventPlayer);
        mod.DisplayNotificationMessage(msg);
    }
    ```
=== "Strings.json"
    ```json
    {
      "died": "{} killed {}!"
    }
    ```

![Screen capture of player dying](../../img/OnPlayerDied_example.gif)

## See Also

- [`OnPlayerDamaged`](./OnPlayerDamaged.md)
- [`OnMandown`](./OnMandown.md)
- [`ForceRevive`](../functions/ForceRevive.md)
- [`OnPlayerDeployed`](./OnPlayerDeployed.md)
