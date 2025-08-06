---
title: Pipes & Networks
permalink: /pipes/
nav_order: 4
---

# 🔄 Pipes & Networks

**Deepslate Industries** includes a modular, direction-aware piping system for automation and logistics. There are currently three core types of pipes:

---

## 📦 Item Pipes

Item Pipes allow you to transport items between machines, inventories, and containers.

- 🔌 **Connections**:
  - Automatically connect to chests, hoppers, and machine inventories.
  - Use a **Wrench** to toggle extraction mode on any pipe face.

- ⚙️ **Functionality**:
  - Items are extracted in batches (default: 16 per tick).
  - Uses an internal pathfinding system to find the closest valid destination.
  - Smartly avoids loops and redundant insertions.

- 🧠 **Special Logic**:
  - Does **not** insert into the source inventory it extracts from.
  - Supports double chests, sided inventories, and priority logic (coming soon).

---

## ⚡ Energy Pipes

Energy Pipes transfer **Redstone Flux (RF)** from power sources to machines.

- 🔋 **Usage**:
  - Connect a power source (e.g., Basic Generator) to any compatible machine.
  - Supports Tech Reborn’s energy API under the hood.

- 🔄 **Flow Direction**:
  - Energy flows from output → input using smart BFS-based logic.
  - Wrenching a pipe will **not** affect energy flow (all directions enabled by default).

---

## 💧 Fluid Pipes (WIP)

Fluid Pipes are currently in development.

- 🧪 Will support fluids from standard Minecraft tanks and modded fluid containers.
- 🛠 Integration with other fluid-based machines is planned in future versions.

---

## 🛠 Network System

All pipes utilize a **Pipe Network Manager** for efficient routing:

- 🔎 **Pathfinding**:
  - Breadth-first search (BFS) to locate valid endpoints.
  - Respects directionality, filters (future), and extraction cooldowns.

- ♻️ **Dynamic Updating**:
  - Pipes refresh their network when placed, broken, or wrenched.
  - No manual chunkloader or world reset needed.

---

Return to [Home](index.md) or check out [Machines](machines.md).
