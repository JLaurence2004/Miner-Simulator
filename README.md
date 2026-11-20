# Miner Simulator

**A Mining Simulation Game Based on CPU Scheduling Algorithms**

Miner Simulator is a game developed using Godot Engine that demonstrates fundamental CPU scheduling concepts through an interactive mining and resource-management environment.

Players control a miner, collect different types of ores, manage inventories, and process resources using a furnace that implements two CPU scheduling algorithms: **First Come, First Served (FCFS)** and **Non-Preemptive Priority Scheduling (NPPS)**.

Each ore has a predefined Burst Time (BT), representing its processing duration, and a corresponding coin value awarded upon successful processing.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Downloads and Installation](#downloads-and-installation)
- [Source Code Setup](#source-code-setup)
- [Game Controls](#game-controls)
- [Gameplay Instructions](#gameplay-instructions)
- [Ore Information](#ore-information)
- [Upgrade System](#upgrade-system)
- [CPU Scheduling Algorithms](#cpu-scheduling-algorithms)
- [Technologies Used](#technologies-used)
- [Project Repository](#project-repository)
- [Developer](#developer)

---

## Project Overview

The primary objective of Miner Simulator is to demonstrate how CPU scheduling algorithms operate through a mining and resource-processing simulation.

The furnace represents the CPU, while collected ores represent processes waiting for execution. Each ore has an assigned Burst Time, coin value, and rarity-based priority.

Players can choose between two scheduling algorithms and observe how different scheduling strategies determine the order in which ores are processed.

## Features

- **Mining System** – Collect different types of ores.
- **Inventory Management** – Manage player, furnace, and mine cart inventories.
- **Ore Processing System** – Process collected ores using their assigned Burst Times.
- **FCFS Scheduling** – Process ores according to their arrival order.
- **NPPS Scheduling** – Process ores according to their rarity-based priority.
- **Upgrade System** – Improve player speed, ore drop chance, furnace speed, and coin gains.
- **Mine Cart System** – Manage resources using the mine cart.
- **Coin System** – Earn currency by successfully processing ores.
- **Windows Support** – Play using the downloadable Windows executable.
- **Open Source Project Files** – Access the Godot project source files.

---

## Downloads and Installation

### Windows (EXE)

A precompiled Windows version is available through the GitHub Releases page.

1. Visit the [Miner Simulator v1.0.0 Release](https://github.com/JLaurence2004/Miner-Simulator/releases/tag/v1.0.0).
2. Locate the Windows game package under the **Assets** section.
3. Download the provided game ZIP file.
4. Extract the downloaded archive.
5. Open the extracted folder.
6. Locate and run the `.exe` file.
7. The game should launch.

**Important:** Keep the executable and its required game resources in the same directory. Do not separate the `.exe` file from its associated `.pck` or required DLL files.

---

## Source Code Setup

Developers who want to inspect, run, or modify the project can download the original Godot project files.

### Downloading the Source Code

1. Visit the [Miner Simulator Source Files](https://github.com/JLaurence2004/Miner-Simulator/blob/main/Miner_Simulator_Files.zip).
2. Download the ZIP archive.
3. Extract the downloaded archive to your preferred directory.

### Opening the Project in Godot

1. Download and install [Godot Engine](https://godotengine.org/).
2. Open the Godot Project Manager.
3. Select **Import**.
4. Browse to the extracted project folder.
5. Locate and select `project.godot`.
6. Click **Import & Edit**.
7. Wait for the project to load.
8. Press `F5` to run the main project.

---

## Game Controls

The following keyboard shortcuts are used to navigate the game and access its interfaces.

| Key | Action |
|:---:|---|
| `W` | Move up |
| `A` | Move left |
| `S` | Move down |
| `D` | Move right |
| `I` | Open Player Inventory |
| `O` | Open Forge/Furnace Inventory |
| `P` | Open Mine Cart Inventory |
| `U` | Open Upgrade Interface |
| `M` / `N` | Toggle Mine Cart movement |
| `TAB` (Hold) | Display upgrade descriptions while the Upgrade Interface is open |
| `L` | Add 1,000 coins (Testing Command) |
| `K` | Reset coin balance to zero (Testing Command) |
| `1` | Select First Come, First Served (FCFS) to process forge ores |
| `2` | Select Non-Preemptive Priority Scheduling (NPPS) to process forge ores |


---

## Gameplay Instructions

### 1. Character Movement

Upon starting the game, the player character spawns in the mining environment.

Use the `W`, `A`, `S`, and `D` keys to navigate the environment and access the available game systems.

### 2. Mining and Resource Collection

Collect ores through the mining system.

Different ores have different rarity levels, processing durations, and coin values.

The collected resources can be managed through the inventory interfaces.

### 3. Inventory Management

Miner Simulator provides three inventory systems:

| Inventory | Shortcut | Description |
|---|:---:|---|
| Player Inventory | `I` | Manages ores and items collected by the player. |
| Forge/Furnace Inventory | `O` | Stores ores designated for processing. |
| Mine Cart Inventory | `P` | Manages resources stored in the mine cart. |

### 4. Ore Processing

Transfer collected ores into the furnace inventory to prepare them for processing.

The furnace uses the selected CPU scheduling algorithm to determine which ore will be processed first.

Each ore has an assigned Burst Time, which determines its processing duration.

Once processing is completed, the corresponding coin value is added to the player's balance.


### 5. Upgrade System

Press `U` to open the Upgrade Interface.

Players can spend their accumulated coins to purchase upgrades that improve mining and processing performance.

Hold `TAB` while the Upgrade Interface is open to view descriptions of the available upgrades.

---

## Ore Information

Each ore has a specific Burst Time (BT), coin value, and rarity level.

| Ore | Rarity | Burst Time (BT) | Coin Value |
|---|---|---:|---:|
| Copper | Common | 3 seconds | 1 |
| Silver | Rare | 14 seconds | 10 |
| Gold | Epic | 17 seconds | 100 |
| Amethyst | Legendary | 20 seconds | 1,000 |

### Ore Priority Ranking

Under Non-Preemptive Priority Scheduling (NPPS), ores are prioritized according to their rarity.

The highest rarity receives the highest processing priority.

**Priority Order (Highest to Lowest):**

1. Amethyst – Legendary
2. Gold – Epic
3. Silver – Rare
4. Copper – Common

---

## Upgrade System

Miner Simulator includes four upgrade categories that improve different aspects of gameplay.

| Upgrade | Description |
|---|---|
| Player Speed | Increases the movement speed of the player character. |
| Ore Chance | Increases the probability of obtaining ores when mining. |
| Furnace Speed | Reduces the Burst Time required to process each ore. |
| Coin Gain per Ore | Increases the amount of coins earned from processed ores. |

These upgrades allow players to improve resource collection, processing efficiency, and overall earnings.

---

## CPU Scheduling Algorithms

Miner Simulator implements two non-preemptive CPU scheduling algorithms through its ore-processing system.

In this simulation:

- **CPU:** Represents the furnace.
- **Processes:** Represent ores waiting to be processed.
- **Burst Time:** Represents the processing duration of each ore.
- **Priority:** Represents the rarity-based importance of each ore.
- **Completion:** Represents the successful processing of an ore.

### 1. First Come, First Served (FCFS)

First Come, First Served is a non-preemptive CPU scheduling algorithm that executes processes according to their arrival order.

**Implementation in Miner Simulator:**

- Ores are processed according to their order in the furnace inventory.
- The earliest eligible ore is processed first.
- Subsequent ores wait until the current ore finishes processing.
- Each ore requires its assigned Burst Time to complete processing.

**Example:**

| Process | Ore | Burst Time |
|---|---|---:|
| P1 | Copper | 3 seconds |
| P2 | Gold | 17 seconds |
| P3 | Silver | 14 seconds |
| P4 | Amethyst | 20 seconds |

**Execution Order:**

`Copper → Gold → Silver → Amethyst`

### 2. Non-Preemptive Priority Scheduling (NPPS)

Non-Preemptive Priority Scheduling executes processes according to their assigned priority levels.

In Miner Simulator, priority is determined by ore rarity. Legendary ores receive the highest priority, while Common ores receive the lowest.

**Implementation in Miner Simulator:**

- Ores are sorted according to their rarity-based priority.
- Higher-priority ores are processed before lower-priority ores.
- Processing cannot be interrupted once an ore begins execution.
- Each ore retains its assigned Burst Time.

**Example:**

| Process | Ore | Priority | Burst Time |
|---|---|---|---:|
| P1 | Copper | Common | 3 seconds |
| P2 | Gold | Epic | 17 seconds |
| P3 | Silver | Rare | 14 seconds |
| P4 | Amethyst | Legendary | 20 seconds |

**Execution Order:**

`Amethyst → Gold → Silver → Copper`

### Algorithm Comparison

| Criteria | FCFS | NPPS |
|---|---|---|
| Scheduling Method | Arrival Order | Rarity-Based Priority |
| Execution Type | Non-Preemptive | Non-Preemptive |
| Priority Consideration | No | Yes |
| Process Interruption | Not allowed | Not allowed |
| Main Characteristic | Executes processes in arrival order | Executes higher-priority processes first |

### Learning Objective

The implementation of FCFS and NPPS provides an interactive representation of CPU scheduling principles.

Through the ore-processing system, players can observe how different scheduling strategies affect process execution order and understand the relationship between Burst Time, process priority, and scheduling policies.

---

## Technologies Used

| Technology | Purpose |
|---|---|
| Godot Engine | Game development |
| GDScript | Game logic and programming |
| Git | Version control |
| GitHub | Source code hosting and project distribution |

---

## Project Repository

| Resource | Link |
|---|---|
| Windows Game | [Download Release v1.0.0](https://github.com/JLaurence2004/Miner-Simulator/releases/tag/v1.0.0) |
| Source Code | [Download Source ZIP](https://github.com/JLaurence2004/Miner-Simulator/blob/main/Miner_Simulator_Files.zip) |
| GitHub Repository | [View Miner Simulator](https://github.com/JLaurence2004/Miner-Simulator) |

---

## Developer

**JLaurence2004**

Bachelor of Science in Computer Science Student

---

*Miner Simulator — An interactive approach to understanding CPU scheduling through game-based simulation.*
