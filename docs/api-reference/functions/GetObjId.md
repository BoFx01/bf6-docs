# GetObjId

Gets the ID of an object.

## Syntax

```typescript
export function GetObjId(modBuilderObject: mod.Object): number;
```

## Parameters

| Parameter          | Type         | Description               |
| ------------------ | ------------ | ------------------------- |
| `modBuilderObject` | `mod.Object` | Game object to get the ID |

## Return Values

| Type     | Description |
| -------- | ----------- |
| `number` | Object ID   |

## Example

```typescript
export async function OnGameModeStarted() {
  const pos = mod.CreateVector(341, 80, -202);
  const icon = mod.SpawnObject(mod.RuntimeSpawn_Common.WorldIcon, pos, mod.CreateVector(0, 0, 0));
  mod.SetWorldIconImage(icon, mod.WorldIconImages.Skull);
  mod.SetWorldIconColor(icon, mod.CreateVector(1, 1, 1));
  mod.EnableWorldIconImage(icon, true);

  // Get the ID of the icon object
  const objId = mod.GetObjId(icon);
  console.log(objId);
}
```