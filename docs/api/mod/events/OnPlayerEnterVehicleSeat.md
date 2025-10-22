# OnPlayerEnterVehicleSeat

This function triggers when a player enters a specific seat in a vehicle. This provides more granular control than `OnPlayerEnterVehicle`, allowing you to differentiate between driver and passenger seats.

## Syntax

```typescript
export function OnPlayerEnterVehicleSeat(
    eventPlayer: mod.Player,
    eventVehicle: mod.Vehicle,
    eventSeat: mod.Object
): void;
```

## Parameters

| Parameter      | Type          | Description                               |
| -------------- | ------------- | ----------------------------------------- |
| `eventPlayer`  | `mod.Player`  | The player who entered the vehicle seat   |
| `eventVehicle` | `mod.Vehicle` | The vehicle containing the seat           |
| `eventSeat`    | `mod.Object`  | The specific seat object that was entered |

## Example

=== "Script.ts"
    ```typescript
    export function OnPlayerEnterVehicleSeat(
        eventPlayer: mod.Player,
        eventVehicle: mod.Vehicle,
        eventSeat: mod.Object
    ) {
      const seatNum = mod.GetPlayerVehicleSeat(eventPlayer);
      // Display message stating if player is driver or passenger
      if (seatNum == 0) {
        const msg = mod.Message(mod.stringkeys.veh_driver, eventPlayer);
        mod.DisplayNotificationMessage(msg, eventPlayer);
      } else {
        const msg = mod.Message(mod.stringkeys.veh_pax, eventPlayer);
        mod.DisplayNotificationMessage(msg, eventPlayer);
      }
    }
    ```
=== "Strings.json"
    ```json
    {
      "veh_driver": "{} is now the driver.",
      "veh_pax": "{} is a passenger."
    }
    ```

![Screen recording of player changing seats](../../../img/OnPlayerEnterVehicleSeat_example.gif)

## See Also

- [`OnPlayerEnterVehicle`](./OnPlayerEnterVehicle.md) - Triggers when a player enters any vehicle seat
- [`OnPlayerExitVehicle`](./OnPlayerExitVehicle.md) - Triggers when a player exits a vehicle
- [`OnPlayerExitVehicleSeat`](./OnPlayerExitVehicleSeat.md) - Triggers when a player exits a specific vehicle seat
