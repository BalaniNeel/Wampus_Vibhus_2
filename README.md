# Wampus

A JavaFX-based visual adaptation of the classic text adventure Hunt the Wumpus. Built with Maven, the game renders a 2D hexagonal cave map generated from CSV files and provides rich UI feedback for movement, hazards, and strategy.

- Repository: [NeelBalani/Wampus_Vibhus_2](https://github.com/NeelBalani/Wampus_Vibhus_2)
- Primary language: Java
- Language composition: Java (90.8%), CSS (9.2%)

## Table of Contents
- [Overview](#overview)
- [Awards](#awards)
- [Key Features](#key-features)
- [Game Content](#game-content)
- [How It Works](#how-it-works)
- [Gameplay & Controls](#gameplay--controls)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Build and Run](#build-and-run)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview
Wampus is a scalable, JavaFX-based GUI game developed for Microsoft’s annual Hunt the Wumpus Competition (a high school game design contest). It modernizes the original text-based mechanics into an interactive, visually navigable cave system composed of hexagonal rooms.

The game loads cave layouts and gameplay data from CSV files, supports smooth navigation, and visually indicates valid moves, hazards, and player position. It applies object-oriented principles to keep cave generation, gameplay logic, UI, trivia, and currency modular and extensible.

## Awards
- Microsoft’s People’s Choice Award — Microsoft’s annual Hunt the Wumpus Competition (high school game design).

## Key Features
- JavaFX UI with CSS styling for a responsive, modern interface.
- 2D hexagonal cave map rendered from CSV files.
- Visual indicators for:
  - Player position
  - Valid moves
  - Hazards (e.g., Wumpus proximity, traps)
- Advanced gameplay mechanics:
  - Wumpus movement and randomized hidden hazards
  - Hint system to assist strategic planning
  - Path tracking and a game history log for replayability
  - Trivia and currency systems integrated into gameplay
- Externalized game data:
  - Cave layouts and trivia questions loaded from files to simplify iteration and customization
- Clean, modular code structure using OOP for maintainability and scalability.

## Game Content
The game includes three CSV-based cave maps:
- tutorial.csv (Tutorial)
- map1.csv (Map 1)
- map2.csv (Map 2)

These files define the layout and connections of hexagonal rooms and are read at startup to construct the cave.

## How It Works
- CSV-driven cave generation:
  - Each CSV encodes rooms (hex cells) and their connections.
  - On load, the game parses the CSV to instantiate Java objects representing the cave (“Caves”) and hexagonal rooms.
- Rendering and UI:
  - JavaFX draws the hex grid and overlays stateful indicators for current position, valid moves, and hazards.
  - CSS customizes visual themes and state highlights.
- Game systems:
  - Movement rules enforce valid transitions across hex neighbors.
  - Wumpus behavior and hazards are randomized each run to keep play sessions fresh.
  - Trivia and currency modules introduce decision-making layers and rewards.
  - A history log tracks moves and outcomes; path tracing supports post-game review.
  - Hint logic suggests strategic options without removing challenge.

## Gameplay & Controls
- Navigate between adjacent hex rooms using the UI controls.
- Watch for visual cues showing:
  - Where you can move next (valid moves)
  - Nearby dangers (hazard indicators)
  - Your current location
- Use hints strategically and manage currency while tackling trivia challenges.
- Track your path and history to refine your approach across runs.

## Project Structure
Top-level layout:

```
.
├── .gitattributes
├── .gitignore
├── .idea/              # IntelliJ project settings
├── .mvn/               # Maven Wrapper support files
├── .vscode/            # VS Code settings
├── .windsurfrules
├── mvnw                # Maven Wrapper (Unix/macOS)
├── mvnw.cmd            # Maven Wrapper (Windows)
├── pom.xml             # Maven configuration (dependencies, plugins)
├── src/                # Java and resources (UI, CSS, data)
├── wampus/             # Project/module files
└── wampus.iml          # IntelliJ module file
```

Key files and folders:
- `pom.xml`: Maven project descriptor.
- `mvnw` / `mvnw.cmd`: Maven Wrapper scripts.
- `src/`: Java source and application resources (JavaFX, CSS, CSVs).
- `wampus/`: Additional project-specific code/resources.

## Getting Started

### Prerequisites
- Java Development Kit (JDK) 17 or later is recommended.
- Git (to clone the repository).

Verify your Java installation:
```bash
java -version
javac -version
```

### Clone the repository
```bash
git clone https://github.com/NeelBalani/Wampus_Vibhus_2.git
cd Wampus_Vibhus_2
```

## Build and Run

This project uses the Maven Wrapper, so you can build and run without a global Maven install.

### Build
```bash
# macOS/Linux
./mvnw clean package

# Windows
mvnw.cmd clean package
```

Artifacts will be generated under `target/`.

### Run
Depending on configuration, run one of the following:

- If an executable JAR is produced:
```bash
java -jar target/<artifactId>-<version>.jar
```

- Using the Maven Exec plugin (replace with your main class):
```bash
# macOS/Linux
./mvnw exec:java -Dexec.mainClass="com.example.Main"

# Windows
mvnw.cmd exec:java -Dexec.mainClass="com.example.Main"
```

- From an IDE: set the project SDK to your installed JDK and run the main class.

Note: If using JavaFX modules directly, ensure your Maven `pom.xml` includes JavaFX dependencies. If launching manually without Maven, you may need appropriate `--module-path` and `--add-modules` JVM arguments for OpenJFX.

## Testing
```bash
# macOS/Linux
./mvnw test

# Windows
mvnw.cmd test
```

## Contributing
Contributions are welcome!
1. Fork the repository.
2. Create a feature branch:
   - `git checkout -b feat/your-feature-name`
3. Commit your changes:
   - `git commit -m "feat: add your feature"`
4. Push the branch:
   - `git push origin feat/your-feature-name`
5. Open a pull request describing your changes.

Please follow conventional commit messages when possible (`feat:`, `fix:`, `docs:`, `chore:`, etc.).

## License
No license information is currently provided. If you plan to use or distribute this code, please add an appropriate open-source license (e.g., MIT, Apache-2.0) or clarify usage terms.

## Contact
Co-Creaters: [vib-s](https://github.com/vib-s), [NeelBalani](https://github.com/NeelBalani), [pranavmullakkal](https://github.com/pranavmullakkal)

For questions or suggestions, please open an issue in the repository.
