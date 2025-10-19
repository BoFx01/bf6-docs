# OnPlayerDeployed

This function triggers when a player has been deployed into the game world. This event occurs after a player spawns and is useful for initializing player-specific settings, granting items, or setting up player states at the start of their deployment.

## Syntax

```typescript
export function OnPlayerDeployed(eventPlayer: mod.Player): void;
```

## Parameters

| Parameter   | Type       | Description                                          |
| ----------- | ---------- | ---------------------------------------------------- |
| eventPlayer | mod.Player | The player who has been deployed into the game world |

## Example

=== "Script.ts"
    ```typescript
    // Give players a welcome message and starting equipment when they deploy
    export async function OnPlayerDeployed(eventPlayer: mod.Player) {
      // Display welcome message
      const welcomeMsg = mod.Message(mod.stringkeys.welcome_player, eventPlayer);
      mod.DisplayNotificationMessage(welcomeMsg, eventPlayer);
    }
    ```
=== "Strings.json"
    ```json
    {
      "welcome_player": "Welcome, {}!"
    }
    ```

![Example of in-game message when player deploys](../../img/OnPlayerDeployed_example.gif)

## See Also

- [`OnPlayerUndeploy`](./OnPlayerUndeploy.md)