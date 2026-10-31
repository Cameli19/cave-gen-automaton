# cave-gen-automaton
 
A small Rust project that uses simple rules to create Game of Life patterns and cave maps.

## About

This project uses a grid of cells to create different patterns and cave-like levels. Each cell is either alive or dead. The cells follow a set of rules based on their eight neighboring cells. As the rules repeat, interesting patterns begin to appear.

The same program can create two different results just by changing the rules:
 
- **Game of Life (B3/S23):** Creates patterns that can stay still, blink on and off, or move across the grid.
- **Cave Generation (B5678/S5678):** Turns random cells into cave-like maps with open spaces, rooms, and tunnels.
The goal is to show how simple rules can create more complex results without telling each cell what the final map should look like.

## Planned Features
 
- **Rule engine:** Run different cellular automata rules using B/S notation.
- **Game of Life:** Create and explore classic patterns.
- **Cave generation:** Turn random grids into cave-like maps.
- **Room detection:** Find connected open spaces and keep the largest room.
- **Level building:** Add a starting point, exit, shortest path, and treasures.
- **Random seed:** Use the same seed to recreate the same starting grid.
- **Output:** Display maps in the terminal and save them as PNG images.

## How It Works
 
Each cell looks at its eight neighbors and follows the selected rule.
 
For example, `B3/S23` means:
 
- An empty cell becomes alive if exactly 3 neighbors are alive.
- A living cell stays alive if it has 2 or 3 living neighbors.
Every cell updates at the same time. The process repeats for several rounds, and new patterns begin to form.
 
## Requirements
 
- Rust 
- Cargo

## Getting Started
 
Clone the repository:
 
```
git clone https://github.com/Cameli19/cave-gen-automaton.git
cd cave-gen-automaton
```
 
Build the project:
 
```
cargo build
```
 
Run the tests:
 
```
cargo test
```
 
Run the program:
 
```
cargo run
```
 
## Project Structure
 
```
cave-gen-automaton/
├── src/
│   ├── lib.rs        # Library entry point and documentation
│   ├── rule.rs       # Reads and handles the rules
│   ├── grid.rs       # Creates and updates the grid
│   ├── rooms.rs      # Finds connected rooms
│   ├── level.rs      # Adds the start, exit, path, and treasures
│   ├── render.rs     # Displays and saves the maps
│   └── main.rs       # Runs the program
├── tests/
├── Cargo.toml
├── proposal.pdf      # Project proposal
├── LICENSE-MIT
└── LICENSE-APACHE
```
 
## Built With
 
- **Rust:** Main programming language.
- **rand:** Creates random starting grids.
- **clap:** Handles command-line options.
- **image:** Saves the maps as PNG files.

## Project Status
 
This project is currently under development. More features will be added as the project grows. The final version of this README will describe what was built, how it works, what did not work, and what I learned.
 
## Author
 
[Camellia Tran] ([Cameli19](https://github.com/Cameli19))
 
## License
 
Licensed under either of
 
- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE))
- MIT license ([LICENSE-MIT](LICENSE-MIT))
at your option.