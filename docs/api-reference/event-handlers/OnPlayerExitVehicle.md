# OnPlayerExitVehicle

This function triggers when a player exits a vehicle. Use this event to handle post-vehicle logic, remove vehicle-specific effects, or track when players leave vehicles.

## Syntax

```typescript
export function OnPlayerExitVehicle(eventPlayer: mod.Player, eventVehicle: mod.Vehicle): void;
```

## Parameters

| Parameter      | Type          | Description                       |
| -------------- | ------------- | --------------------------------- |
| `eventPlayer`  | `mod.Player`  | The player who exited the vehicle |
| `eventVehicle` | `mod.Vehicle` | The vehicle that was exited       |

## Example

=== "Script.ts"
    ```typescript
    export function OnPlayerExitVehicle(eventPlayer: mod.Player, eventVehicle: mod.Vehicle) {
      const msg = mod.Message(mod.stringkeys.veh_exit, eventPlayer);
      mod.DisplayNotificationMessage(msg, eventPlayer);
      
      const vehicleId = mod.GetObjId(eventVehicle);
      console.log(`Player exited vehicle ID: ${vehicleId}`);
    }
    ```
=== "Strings.json"
    ```json
    {
      "veh_exit": "{} exited a vehicle."
    }
    ```

![Screen recording of player exiting vehicle](../../img/OnPlayerExitVehicle_example.gif)

## See Also

- [`OnPlayerEnterVehicle`](./OnPlayerEnterVehicle.md) - Triggers when a player enters a vehicle
- [`OnPlayerEnterVehicleSeat`](./OnPlayerEnterVehicleSeat.md) - Triggers when a player enters a specific vehicle seat
- [`OnPlayerExitVehicleSeat`](./OnPlayerExitVehicleSeat.md) - Triggers when a player exits a specific vehicle seat


