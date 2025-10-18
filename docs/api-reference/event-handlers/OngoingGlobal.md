# OngoingGlobal

The `OngoingGlobal` function is an event handler that is called every tick in the background while the server is active. It operates independently of player actions and is ideal for implementing:

- Periodic server-wide notifications or announcements
- Continuous monitoring of global game state
- Scheduled events or timed actions
- Background tasks that need to run throughout the server's lifetime

## Syntax

```typescript
export function OngoingGlobal(): void;
```
