# GetAreaTrigger

Gets the [`AreaTrigger`](../types/AreaTrigger.md) by `id`.

## Syntax

```typescript
export function GetAreaTrigger(areaTriggerNumber: number): AreaTrigger;
```

## Parameters

| Parameter | Type | Description |
| --------- | --- | --- |
| `areaTriggerNumber` | `number` | Number ID of the area trigger to get. |

## Example

```typescript
// Enable a trigger area
export async function OnGameModeStarted() {
  console.log("Game mode started")
  const areaTrigger = mod.GetAreaTrigger(500); // ID as defined in the Godot level editor
  mod.EnableAreaTrigger(areaTrigger, true);
}
```

## See Also
- [`AreaTrigger`](../types/AreaTrigger.md)