# Wait

The `Wait` function suspends the execution of the current async function for the specified number of seconds. This is useful for creating delays between actions, implementing cooldowns, or scheduling periodic tasks.

## Syntax

```typescript
export function Wait(n: number): Promise<void>;
```

### Parameters

- `n` (number): The duration to wait in seconds. Can be a decimal value for sub-second precision (e.g., `0.5` for 500 milliseconds).

### Returns

A `Promise<void>` that resolves after the specified duration has elapsed.

## Example

```typescript
// Wait for 5 seconds before continuing
await mod.Wait(5);
```

## Common Mistakes

- **Missing `await`**: Forgetting to use `await` will cause the function to continue immediately without waiting
  ```typescript
  // ❌ Incorrect - won't actually wait
  mod.Wait(5);
  
  // ✅ Correct - properly waits
  await mod.Wait(5);
  ```

- **Using in non-async functions**: The `Wait` function can only be used within async functions
  ```typescript
  // ❌ Won't work
  function RegularFunction() {
    await mod.Wait(5); // Error: await can only be used in async functions
  }
  
  // ✅ Correct
  async function AsyncFunction() {
    await mod.Wait(5);
  }
  ```
