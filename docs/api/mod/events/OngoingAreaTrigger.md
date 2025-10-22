# OngoingAreaTrigger

The `OngoingAreaTrigger` function is called continuously for every area trigger that exists in the game. This is an ongoing event that runs repeatedly, allowing you to check conditions and perform actions specific to each individual area trigger.

This function is useful for:
- Monitoring the state of area triggers
- Performing continuous checks on area trigger properties
- Implementing custom behavior that needs to evaluate regularly for each area trigger

## Syntax

```typescript
export function OngoingAreaTrigger(eventAreaTrigger: mod.AreaTrigger): void;
```

## Parameters

| Parameter          | Type              | Description                                                          |
| ------------------ | ----------------- | -------------------------------------------------------------------- |
| `eventAreaTrigger` | `mod.AreaTrigger` | The area trigger entity that this event is currently evaluating for. |

## See Also
- [AreaTrigger](../types/AreaTrigger.md)
- [EnableAreaTrigger](../functions/EnableAreaTrigger.md)
- [GetAreaTrigger](../functions/GetAreaTrigger.md)
- [OnPlayerEnterAreaTrigger](./OnPlayerEnterAreaTrigger.md)
- [OnPlayerExitAreaTrigger](./OnPlayerExitAreaTrigger.md)