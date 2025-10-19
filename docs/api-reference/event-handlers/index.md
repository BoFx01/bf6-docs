# Event Handlers

!!! warning "Work in Progress"

    This documentation is a work in progress. Contributions are encouraged. Only pages with a checkmark are complete.

## Functions

### Game Mode Events

- [x] [OnGameModeStarted](./OnGameModeStarted.md)
- [x] [OnGameModeEnding](./OnGameModeEnding.md)
- [ ] [OnTimeLimitReached](./OnTimeLimitReached.md)

### Player Events

**Deployment**

  - [x] [OnPlayerDeployed](./OnPlayerDeployed.md)
  - [x] [OnPlayerUndeploy](./OnPlayerUndeploy.md)
  - [x] [OnPlayerJoinGame](./OnPlayerJoinGame.md)
  - [x] [OnPlayerLeaveGame](./OnPlayerLeaveGame.md)
  - [ ] [OnPlayerSwitchTeam](./OnPlayerSwitchTeam.md)

**Area/Object Interaction**

  - [x] [OnPlayerEnterAreaTrigger](./OnPlayerEnterAreaTrigger.md)
  - [x] [OnPlayerExitAreaTrigger](./OnPlayerExitAreaTrigger.md)
  - [ ] [OnPlayerEnterCapturePoint](./OnPlayerEnterCapturePoint.md)
  - [ ] [OnPlayerExitCapturePoint](./OnPlayerExitCapturePoint.md)
  - [ ] [OnPlayerInteract](./OnPlayerInteract.md)

**Combat**

  - [ ] [OnPlayerDamaged](./OnPlayerDamaged.md)
  - [ ] [OnPlayerDied](./OnPlayerDied.md)
  - [ ] [OnPlayerEarnedKill](./OnPlayerEarnedKill.md)
  - [ ] [OnPlayerEarnedKillAssist](./OnPlayerEarnedKillAssist.md)
  - [ ] [OnMandown](./OnMandown.md)
  - [ ] [OnRevived](./OnRevived.md)

**Vehicle Interaction**

  - [ ] [OnPlayerEnterVehicle](./OnPlayerEnterVehicle.md)
  - [ ] [OnPlayerEnterVehicleSeat](./OnPlayerEnterVehicleSeat.md)
  - [ ] [OnPlayerExitVehicle](./OnPlayerExitVehicle.md)
  - [ ] [OnPlayerExitVehicleSeat](./OnPlayerExitVehicleSeat.md)

**Other Player Events**

  - [ ] [OnPlayerUIButtonEvent](./OnPlayerUIButtonEvent.md)
  - [ ] [OnSpawnerSpawned](./OnSpawnerSpawned.md)
  - [ ] [OnRayCastHit](./OnRayCastHit.md)
  - [ ] [OnRayCastMissed](./OnRayCastMissed.md)

### Objective Events

**Capture Points**

  - [ ] [OnCapturePointCaptured](./OnCapturePointCaptured.md)
  - [ ] [OnCapturePointCapturing](./OnCapturePointCapturing.md)
  - [ ] [OnCapturePointLost](./OnCapturePointLost.md)

**MCOM Stations**

  - [ ] [OnMCOMArmed](./OnMCOMArmed.md)
  - [ ] [OnMCOMDefused](./OnMCOMDefused.md)
  - [ ] [OnMCOMDestroyed](./OnMCOMDestroyed.md)

### AI Events

**Movement**

  - [ ] [OnAIMoveToFailed](./OnAIMoveToFailed.md)
  - [ ] [OnAIMoveToRunning](./OnAIMoveToRunning.md)
  - [ ] [OnAIMoveToSucceeded](./OnAIMoveToSucceeded.md)

**Parachuting**

  - [ ] [OnAIParachuteRunning](./OnAIParachuteRunning.md)
  - [ ] [OnAIParachuteSucceeded](./OnAIParachuteSucceeded.md)

**Waypoint Idle**

  - [ ] [OnAIWaypointIdleFailed](./OnAIWaypointIdleFailed.md)
  - [ ] [OnAIWaypointIdleRunning](./OnAIWaypointIdleRunning.md)
  - [ ] [OnAIWaypointIdleSucceeded](./OnAIWaypointIdleSucceeded.md)

### Vehicle Events

- [ ] [OnVehicleDestroyed](./OnVehicleDestroyed.md)
- [ ] [OnVehicleSpawned](./OnVehicleSpawned.md)

### Ongoing/Continuous Events

!!! warning

    These are advanced event handlers and are not recommended for beginners.

**Global & Environmental**

  - [x] [OngoingGlobal](./OngoingGlobal.md)
  - [x] [OngoingAreaTrigger](./OngoingAreaTrigger.md)
  - [ ] [OngoingScreenEffect](./OngoingScreenEffect.md)
  - [ ] [OngoingWorldIcon](./OngoingWorldIcon.md)

**Objective-Related**

  - [ ] [OngoingCapturePoint](./OngoingCapturePoint.md)
  - [ ] [OngoingMCOM](./OngoingMCOM.md)
  - [ ] [OngoingSector](./OngoingSector.md)
  - [ ] [OngoingInteractPoint](./OngoingInteractPoint.md)

**Spawning Systems**

  - [ ] [OngoingSpawner](./OngoingSpawner.md)
  - [ ] [OngoingSpawnPoint](./OngoingSpawnPoint.md)
  - [ ] [OngoingEmplacementSpawner](./OngoingEmplacementSpawner.md)
  - [ ] [OngoingVehicleSpawner](./OngoingVehicleSpawner.md)

**Entities**

  - [ ] [OngoingPlayer](./OngoingPlayer.md)
  - [ ] [OngoingTeam](./OngoingTeam.md)
  - [ ] [OngoingVehicle](./OngoingVehicle.md)
  - [ ] [OngoingHQ](./OngoingHQ.md)
  - [ ] [OngoingWaypointPath](./OngoingWaypointPath.md)