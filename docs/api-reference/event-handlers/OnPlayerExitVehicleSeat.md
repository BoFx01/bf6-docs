# OnPlayerExitVehicleSeat

This function triggers when a player exits a specific seat in a vehicle. This provides detailed information about which seat the player left, useful for seat-specific logic.

## Syntax

```typescript
export function OnPlayerExitVehicleSeat(
    eventPlayer: mod.Player,
    eventVehicle: mod.Vehicle,
    eventSeat: mod.Object
): void;
```

## Parameters

| Parameter      | Type          | Description                              |
| -------------- | ------------- | ---------------------------------------- |
| `eventPlayer`  | `mod.Player`  | The player who exited the vehicle seat   |
| `eventVehicle` | `mod.Vehicle` | The vehicle containing the seat          |
| `eventSeat`    | `mod.Object`  | The specific seat object that was exited |

## See Also

- [`OnPlayerEnterVehicle`](./OnPlayerEnterVehicle.md) - Triggers when a player enters a vehicle
- [`OnPlayerEnterVehicleSeat`](./OnPlayerEnterVehicleSeat.md) - Triggers when a player enters a specific vehicle seat
- [`OnPlayerExitVehicle`](./OnPlayerExitVehicle.md) - Triggers when a player exits a vehicle