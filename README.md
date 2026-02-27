# Console Icon Consuming Game

A simple C# console game where the player moves around the screen, collects foods, and gains temporary effects based on what they eat.

## Gameplay

Move the player using the arrow keys (← ↑ → ↓). Different food items appear randomly on the screen.

| Food | Player State | Effect |
|------|--------------|--------|
| `@@@@@` | `('-')` | No effect |
| `$$$$$` | `(^-^)` | Increased movement speed |
| `#####` | `(X_X)` | Player freezes briefly |

The player’s appearance changes to match the food consumed, and each state affects movement until it resets.

## Features

- Arrow‑key movement with boundary clamping  
- Random food spawning  
- Collision detection  
- Temporary freeze effect when `(X_X)`  
- Optional speed boost when `(^-^)`  
- Automatic reset to normal state after effects end  

## How It Works

- **Move()** handles input and movement speed  
- **ConsumedTheFood()** checks collisions  
- **ChangePlayer()** updates the player’s appearance  
- **ShouldFreeze()** and **FreezePlayer()** manage the freeze effect  
- **MoveSpeed()** adjusts movement speed based on the current state  

## Running the Game

Compile and run with:

```bash
dotnet run