<div align="center">

# 🏺 ClayPOT

## A Custom-Built C++ Educational 2D Game Engine

<img src="./Resources/logos/logo.png" alt="ClayPOT Logo" width="300"/>

**Learn Game Engine Architecture • Master DSA & Software Engineering • Build RPG Games**

<p>
  <a href="#features"><strong>Features</strong></a> •
  <a href="#quick-start"><strong>Quick Start</strong></a> •
  <a href="#architecture"><strong>Architecture</strong></a> •
  <a href="#documentation"><strong>Documentation</strong></a> •
  <a href="#contributing"><strong>Contributing</strong></a>
</p>

</div>

---

## 📖 Project Overview

**ClayPOT** is an educational 2D game engine prototype developed in C++ to demonstrate the fundamentals of game engine architecture, advanced data structures, and software engineering principles. This project bridges the gap between theoretical computer science concepts and practical game development by implementing:

- **Entity Component System (ECS)** architecture for flexible object management
- **Behaviour Trees** for intelligent NPC AI and decision-making
- **A* Pathfinding Algorithm** for optimal path calculation and navigation
- **Grid-Based Tile System** for map management and collision detection
- **AABB Collision Detection** for efficient physics simulation

ClayPOT serves both as an **educational tool for learning engine development** and as a **functional game engine** capable of creating RPG-style games. It demonstrates real-world applications of Data Structures & Algorithms (DSA), Design Patterns, and Software Engineering principles in a practical, game development context.

### Why ClayPOT?

Traditional game engines like Unreal and Unity abstract away the underlying complexity. **ClayPOT reveals the architecture**, allowing developers to:

- Understand how game engines work at a fundamental level
- Apply DSA concepts in real-world scenarios
- Learn professional C++ development practices
- Prototype and develop custom game mechanics

---

## ✨ Key Features

<table align="center">
  <tr>
    <td width="50%">
      <h3>🎮 Core Engine Systems</h3>
      <ul>
        <li>High-performance 2D sprite rendering (SFML)</li>
        <li>Entity Component System (ECS)</li>
        <li>State management (Menu → Game → Editor)</li>
        <li>Frame-based sprite animation</li>
      </ul>
    </td>
    <td width="50%">
      <h3>🤖 AI & Pathfinding</h3>
      <ul>
        <li>Behaviour Tree framework</li>
        <li>A* algorithm implementation</li>
        <li>Blackboard pattern communication</li>
        <li>Intelligent NPC behavior</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <h3>🛠 Game Development Tools</h3>
      <ul>
        <li>Built-in tile-based level editor</li>
        <li>Automated resource management</li>
        <li>AABB collision detection</li>
        <li>Character stats/inventory system</li>
      </ul>
    </td>
    <td width="50%">
      <h3>🏗 Architecture & Design</h3>
      <ul>
        <li>Modular component-based design</li>
        <li>Template metaprogramming</li>
        <li>Professional design patterns</li>
        <li>Efficient spatial partitioning</li>
      </ul>
    </td>
  </tr>
</table>

---

## 🎯 Technologies & Dependencies

<div align="center">

| Component | Technology | Version |
|:-:|:-:|:-:|
| **Language** | C++ | C++17 |
| **Graphics** | SFML | 2.5+ |
| **IDE** | Visual Studio | 2022 |
| **Platform** | Windows | 10+ (x64) |

**All required runtime dependencies are included with the executable.**

</div>

---

## 🚀 Quick Start

### <div align="center"> Option 1: Run Pre-Built Executable (Recommended) </div>

```
1. Navigate to: Combined_Project/ClayPOT_exe/
2. Ensure all .dll files are in the same folder as ClayPOT.exe
3. Double-click ClayPOT.exe
4. Allow Windows security prompt if shown
```

> ✅ **Works immediately** • No installation required • All dependencies included

### <div align="center"> Option 2: Build from Source </div>

```bash
# Clone the repository
git clone https://github.com/yourusername/ClayPOT.git
cd ClayPOT

# Open solution in Visual Studio 2022
# Set Build Configuration to "Release"
# Build (Ctrl+Shift+B)
```

---

## 📋 How to Use the Engine

### Launching the Application

When you launch `ClayPOT.exe`, you'll see the **Main Menu**:

```
┌─────────────────────────────────┐
│      ClayPOT Game Engine        │
│                                 │
│      ► Play Game                │
│      ► Level Editor             │
│      ► Settings                 │
│      ► Exit                     │
└─────────────────────────────────┘
```

### File Menu Options

Click **File** button in the menu to access:

| Option | Function |
|--------|----------|
| **New Game** | Start a fresh gameplay session |
| **Load Game** | Resume from a saved save point |
| **Level Editor** | Create and edit custom maps |
| **Settings** | Configure graphics, audio, controls |
| **Exit** | Close the engine |

### Keyboard Controls

#### Movement & Interaction
- **WASD** or **Arrow Keys**: Move player
- **Space**: Interact with NPCs and objects
- **E**: Secondary action

#### Combat
- **Left Click**: Attack in facing direction
- **Right Click**: Use special ability

#### Editor Mode
- **Tab**: Toggle tile selector
- **Left Click**: Place tiles
- **Right Click**: Remove tiles
- **WASD**: Pan camera
- **U/I**: Adjust tile render layer
- **Scroll**: Zoom camera

---

## 📂 Repository Structure

<div align="center">

```
ClayPOT/
│
├── 📁 Combined_Project/
│   ├── 📁 ClayPOT_exe/           ← Ready-to-run executable
│   │   ├── ClayPOT.exe           (double-click to launch)
│   │   ├── *.dll                 (dependencies)
│   │   └── Resources/            (assets)
│   │
│   └── 📁 src_code/              ← Complete source code
│       ├── ClayPOT.sln           (Visual Studio solution)
│       ├── *.h & *.cpp           (implementation files)
│       └── Documentation/        (technical docs)
│
├── README.md                      (this file)
├── LICENSE                        (MIT License)
└── PROJECT_REPORT.md             (full technical report)
```

</div>

---

## 🏗 Architecture Highlights

### Entity Component System (ECS)
```
Entity (GameObject)
├── Position Component
├── Health Component  
├── Sprite Component
└── Behaviour Component
```
Enables flexible composition and data-oriented design.

### Behaviour Trees
```
Root
├── Selector (picks first success)
│   ├── Sequence (all must succeed)
│   │   ├── IsEnemyNear?
│   │   └── AttackEnemy()
│   └── PatrolPath()
```
Provides composable, readable AI decision logic.

### A* Pathfinding
```
Start → [Open Set] → Path Found → Goal
         ↓
    Heuristic (Manhattan Distance)
    ↓
    Optimal Route Calculated
```
Efficient shortest-path calculation for NPC movement.

---

## 🎓 Learning Resources

### Data Structures Implemented
- **Vectors**: Dynamic arrays for entities/components
- **Hash Maps**: O(1) resource and entity lookup
- **Priority Queues**: A* algorithm open set
- **Stacks & Queues**: State and event management
- **Graphs & Trees**: Pathfinding networks and behaviour trees
- **Spatial Grids**: Collision optimization

### Algorithms Demonstrated
- **A* Search**: Optimal pathfinding with heuristics
- **Depth-First Search (DFS)**: Behaviour tree traversal
- **AABB Intersection**: Collision detection
- **Spatial Culling**: Rendering optimization
- **Graph Generation**: Tilemap navigation conversion

---

## 🔧 Troubleshooting

| Problem | Solution |
|---------|----------|
| **"DLL not found"** | Keep all `.dll` files with `ClayPOT.exe` |
| **Visual C++ Missing** | Install [VC++ 2022 Redistributable](https://support.microsoft.com/en-us/help/2977003) |
| **Crashes on startup** | Run as Administrator, update Windows |
| **Low FPS** | Reduce graphics quality in Settings |

---

## 📚 Documentation

- 📄 **[Full Project Report](./PROJECT_REPORT.md)** - Comprehensive technical documentation
- 📖 **[Architecture Guide](./src_code/Documentation/)** - System design and implementation details
- 🎮 **[Developer Guide](./src_code/Documentation/)** - Building and extending the engine
- 🔍 **[Algorithm Explanations](./src_code/Documentation/)** - In-depth algorithm walkthroughs

---

## 🤝 Contributing

We welcome contributions! Here's how:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/YourFeature`
3. **Commit** your changes: `git commit -m 'Add YourFeature'`
4. **Push**: `git push origin feature/YourFeature`
5. **Submit** a Pull Request

### Guidelines
- Follow C++17 standards
- Add comments for complex logic
- Test thoroughly before submitting
- Update documentation as needed

---

## 📜 License

<div align="center">

This project is licensed under the **MIT License** - see [LICENSE](LICENSE) file for details.

You are free to use, modify, and distribute this code with proper attribution.

</div>

---

## 👨‍💻 Author

<div align="center">

**[Your Name]**

[Portfolio](https://yourwebsite.com) • [GitHub](https://github.com/yourusername) • [LinkedIn](https://linkedin.com/in/yourprofile)

</div>

---

## 🎓 Educational Use

**ClayPOT is ideal for:**
- 🎓 Students learning game engine architecture
- 👨‍🏫 Educators teaching DSA and C++ programming
- 💼 Developers building portfolio projects
- 🔬 Researchers exploring game AI systems

---

## 🐛 Found a Bug?

<div align="center">

**[Report an Issue](https://github.com/yourusername/ClayPOT/issues)**

Provide:
- Bug description
- Reproduction steps
- System information
- Expected vs actual behavior

</div>

---

<div align="center">

## ⭐ Show Your Support

If ClayPOT helped you learn or build something awesome, please:
- **Star** ⭐ the repository
- **Watch** 👀 for updates
- **Share** 🔗 with others learning game dev

---

**Made with ❤️ for game developers and computer science enthusiasts**

© 2025 ClayPOT Game Engine

</div>
