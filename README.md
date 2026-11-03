# 🐍 Unity Snake Game

A classic **Snake** game built in **Unity 6** with **C#**. Steer the snake around the grid, eat food to grow longer, and avoid the walls.

## 🎮 Controls

| Key | Action |
|-----|--------|
| **W** | Move up |
| **A** | Move left |
| **S** | Move down |
| **D** | Move right |

## ✨ Features

- Grid-based movement on a fixed timestep (`FixedUpdate`) for consistent speed
- The snake grows by one segment each time it eats
- Food respawns at a random position inside the play area
- Hitting a wall resets the game
- 2D physics triggers for collisions, using tags (`Food`, `Obstacle`, `Player`)

## 🛠️ How it works

| Script | Responsibility |
|--------|----------------|
| `Assets/Snake.cs` | Reads WASD input, moves the head one grid cell per tick, makes each body segment follow the one in front, grows on food and resets on obstacles. Segments are stored in a `List<Transform>`. |
| `Assets/Food.cs` | Picks a random, grid-snapped position inside a `BoxCollider2D` play area and moves when the snake eats it. |
| `Assets/SnakeSegment.prefab` | The body segment that is created each time the snake grows. |

## ▶️ Running the project

1. Install **Unity 6** (editor version `6000.6.4f1` or newer) through Unity Hub.
2. Clone this repository:
   ```bash
   git clone https://github.com/Eduard-11/Unity-Snake-Game.git
   ```
3. In Unity Hub, click **Add → Add project from disk** and choose the cloned folder.
4. Open `Assets/Scenes/Snake.unity` and press **Play**.

## 📚 What I learned

- Unity's game loop (`Start`, `Update`, `FixedUpdate`) and when to use each
- Working with prefabs and instantiating objects at runtime
- 2D colliders, triggers and tags for collision handling
- Managing game state with C# collections

## 🚧 Planned improvements

- Score counter and high score
- Stop the snake from reversing straight into itself
- Self-collision (game over when the snake hits its own body)
- Speed increase as the snake grows
- Playable WebGL build

---

Built by **Eduard Herman**, final-year Bachelor of Computing (Software Engineering) student at Belgium Campus iTversity · [LinkedIn](https://www.linkedin.com/in/eduard-herman-3a65a3230/)
