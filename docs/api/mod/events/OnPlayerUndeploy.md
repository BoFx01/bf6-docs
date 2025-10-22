# OnPlayerUndeploy

This function triggers when a player undeploys from a game. This is useful for handling cleanup logic, tracking player state changes, or applying effects when a player transitions out of a deployed position.

## Syntax

```typescript
export function OnPlayerUndeploy(eventPlayer: mod.Player): void;
```

## Parameters

| Parameter   | Type       | Description                   |
| ----------- | ---------- | ----------------------------- |
| eventPlayer | mod.Player | The player who is undeploying |

## Example

=== "Script.ts"
    ```typescript
    // Track how long players stay deployed
    const deploymentTimes = new Map<number, number>();

    export async function OnPlayerDeployed(eventPlayer: mod.Player) {
      const playerId = mod.GetObjId(eventPlayer);
      deploymentTimes.set(playerId, Date.now());
      console.log(`Player ${playerId} deployed`);
    }

    // Show the player how long they were deployed
    export async function OnPlayerUndeploy(eventPlayer: mod.Player) {
      const playerId = mod.GetObjId(eventPlayer);
      const deployTime = deploymentTimes.get(playerId);
      
      if (deployTime) {
        const duration = (Date.now() - deployTime) / 1000;
        console.log(`Player ${playerId} was deployed for ${duration} seconds`);
        const deployMsg = mod.Message(mod.stringkeys.deploy_time, duration);
        mod.DisplayNotificationMessage(deployMsg, eventPlayer);
        deploymentTimes.delete(playerId);
      }
    }
    ```
=== "Strings.json"
    ```json
    {
      "deploy_time": "You were deployed for {} seconds."
    }
    ```

![Screen recording of player deploying and undeploying](../../../img/OnPlayerUndeploy_example.gif)

## See Also

- [`OnPlayerDeployed`](./OnPlayerDeployed.md)
