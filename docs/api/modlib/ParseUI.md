# ParseUI

This function creates and configures UI widgets from a parameters object. It iterates through the provided parameters and creates UI widgets, returning the last created widget. This allows the UI to be declared using nested objects. [ui_builder](https://github.com/battlefield-portal-community/ui_builder) is a tool that can be used to design UIs visually.

## Syntax

```typescript
export function ParseUI(...params: any[]): mod.UIWidget | undefined;
```

## Parameters

| Parameter | Type    | Description                                        |
| --------- | ------- | -------------------------------------------------- |
| `params`  | `any[]` | Variable number of UI widget configuration objects |

## Return Values

| Type                        | Description                                                                            |
| --------------------------- | -------------------------------------------------------------------------------------- |
| `mod.UIWidget | undefined` | The last UI widget created from the parameters, or undefined if no parameters provided |

## Example

=== "Script.ts"
    ```typescript
    import * as modlib from 'modlib';

    export function OnPlayerDeployed(eventPlayer: mod.Player) {

      const containerPc2x1Widget = modlib.ParseUI(
        {
          name: "Container_PC2X1",
          type: "Container",
          position: [0, 46.88],
          size: [559.74, 69.66],
          anchor: mod.UIAnchor.TopCenter,
          visible: true,
          padding: 0,
          bgColor: [0.0314, 0.0431, 0.0431],
          bgAlpha: 0.5,
          bgFill: mod.UIBgFill.Blur,
          children: [
            {
              name: "Hello World",
              type: "Text",
              position: [0, 0],
              size: [273.91, 57.56],
              anchor: mod.UIAnchor.Center,
              visible: true,
              padding: 0,
              bgColor: [0.2, 0.2, 0.2],
              bgAlpha: 1,
              bgFill: mod.UIBgFill.None,
              textLabel: mod.stringkeys.Hello_World,
              textColor: [1, 1, 1],
              textAlpha: 1,
              textSize: 24,
              textAnchor: mod.UIAnchor.Center
            }
          ]
        }
      ) as mod.UIWidget;

      mod.SetUIWidgetVisible(containerPc2x1Widget, true);
    }
    ```
=== "Strings.json"
    ```json
    {
      "Hello_World": "Hello, world"
    }
    ```

![Screen capture of a UI widget](../../../img/SetUIWidgetVisible_example.png)

## See Also

- [`AddUIContainer`](../mod/functions/AddUIContainer.md)
- [`AddUIButton`](../mod/functions/AddUIButton.md)
- [`SetUIWidgetVisible`](../mod/functions/SetUIWidgetVisible.md)
