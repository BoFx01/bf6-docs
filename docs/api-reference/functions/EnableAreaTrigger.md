# EnableAreaTrigger

Enables or disables an [`AreaTrigger`](../types/AreaTrigger.md). Area triggers must be enabled before events such as [`OnPlayerEnterAreaTrigger`](../event-handlers/OnPlayerEnterAreaTrigger.md) are fired.

## Syntax

```typescript
export function EnableAreaTrigger(areaTrigger: AreaTrigger, enable: boolean): void;
```

## Parameters

| Parameter     | Type              | Description                                              |
| ------------- | ----------------- | -------------------------------------------------------- |
| `areaTrigger` | `mod.AreaTrigger` | The area trigger entity that is being modifed.           |
| `enable`      | `boolean`         | `true` enables the area trigger and `false` disables it. |

## Example

```typescript
// Enable a trigger area
export async function OnGameModeStarted() {
  console.log("Game mode started")
  const areaTrigger = mod.GetAreaTrigger(500);
  mod.EnableAreaTrigger(areaTrigger, true);
}
```

## See Also

- [`AreaTrigger`](../types/AreaTrigger.md)
