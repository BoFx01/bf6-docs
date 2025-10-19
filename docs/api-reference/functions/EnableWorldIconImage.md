# EnableWorldIconImage

Enables or disables the visibility of a world icon's image.

## Syntax

```typescript
export function EnableWorldIconImage(worldIcon: WorldIcon, enableImage: boolean): void;
```

## Parameters

| Parameter     | Type        | Description                                              |
| ------------- | ----------- | -------------------------------------------------------- |
| `worldIcon`   | `WorldIcon` | The world icon object whose image visibility to control. |
| `enableImage` | `boolean`   | `true` to show the icon image, `false` to hide it.       |


## Example

```typescript
export async function OnGameModeStarted() {
  console.log("Game mode started")
  const pos = mod.CreateVector(341, 85, -202);
  const icon = mod.SpawnObject(mod.RuntimeSpawn_Common.WorldIcon, pos, mod.CreateVector(0, 0, 0));
  mod.SetWorldIconImage(icon, mod.WorldIconImages.Skull);
  mod.SetWorldIconColor(icon, mod.CreateVector(1, 1, 1));
  mod.SetWorldIconText(icon, mod.Message(mod.stringkeys.icon_text));

  // Enable icon image and text to show them in the world
  mod.EnableWorldIconImage(icon, true);
  mod.EnableWorldIconText(icon, true);
  console.log(mod.GetObjId(icon));
}
```