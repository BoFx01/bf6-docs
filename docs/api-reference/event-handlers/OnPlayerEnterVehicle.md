# OnPlayerEnterVehicle

This function triggers when a player enters any seat in a vehicle. Use this event to handle vehicle entry logic, apply vehicle-specific effects to players, or track vehicle usage.

## Syntax

```typescript
export function OnPlayerEnterVehicle(eventPlayer: mod.Player, eventVehicle: mod.Vehicle): void;
```

## Parameters

| Parameter      | Type          | Description                        |
| -------------- | ------------- | ---------------------------------- |
| `eventPlayer`  | `mod.Player`  | The player who entered the vehicle |
| `eventVehicle` | `mod.Vehicle` | The vehicle that was entered       |

## Example

=== "Script.ts"
    ```typescript
    export function OnPlayerEnterVehicle(eventPlayer: mod.Player, eventVehicle: mod.Vehicle) {
      const msg = mod.Message(mod.stringkeys.veh_enter, eventPlayer);
      mod.DisplayNotificationMessage(msg, eventPlayer);
      
      const vehicleId = mod.GetObjId(eventVehicle);
      console.log(`Vehicle ID: ${vehicleId}`);
    }
    ```
=== "Strings.json"
    ```json
    {
      "veh_enter": "{} entered a vehicle."
    }
    ```

![Screen recording of player entering vehicle](../../img/OnPlayerEnterVehicle_example.gif)

## See Also

- [`OnPlayerEnterVehicleSeat`](./OnPlayerEnterVehicleSeat.md) - Triggers when a player enters a specific vehicle seat
- [`OnPlayerExitVehicle`](./OnPlayerExitVehicle.md) - Triggers when a player exits a vehicle
- [`OnPlayerExitVehicleSeat`](./OnPlayerExitVehicleSeat.md) - Triggers when a player exits a specific vehicle seat
