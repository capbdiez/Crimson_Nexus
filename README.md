# Crimson Nexus - Game Specification

## Overview
Crimson Nexus is a handcrafted real-time Action Role-Playing Game (ARPG) that immerses players in a living, breathing world where nature and magic intertwine. Set against the backdrop of dimensional rifts connecting our world to a mysterious monster dimension, players must navigate a vibrant open world, confront existential threats, and uncover the truth behind the cosmic phenomena that bind their reality.

## Key Features

### Player Progression System
- **5-Attribute System**: Players level up 5 core stats:
  - **Strength**: Physical damage and stagger
  - **Agility**: Speed and dodge
  - **Intelligence**: Mana pool and critical hits
  - **Health**: HP and passive regeneration
  - **Sorcery**: Magic damage and Area of Effect

- **Dynamic Class Assignment**: 
  - No initial class choice by players
  - Game analyzes stats and combat style in real-time
  - Assigns percentage-based classes (e.g., 80% Mage / 20% Assassin)
  - Base classes: Explorer, Swordsman, Tank, Assassin, Mage, Necromancer

- **Skill System Integration**: Progression drives skill tree unlocks and abilities

### Core Gameplay
- Real-time combat system with player vs. enemies
- Character progression through experience and skill trees
- Inventory management with crafting system
- Exploration of handcrafted open world (50+ square kilometers)
- Interaction with dynamic environmental systems
- Survival-based gameplay mechanics
- Quest system with multiple branching narratives
- Dungeon & Difficulty System with rank-based portal mechanics

### Technical Specifications
- Real-time 60 FPS on modern hardware with Godot Engine
- **2D Pixel Art Style**: Hand-drawn pixel graphics using Godot's Sprite2D and AnimatedSprite nodes
- Dynamic lighting and atmospheric effects with Godot's CanvasItem and LightingEngine
- Comprehensive accessibility features with Godot UI system
- Cloud and local save systems with Godot's FileSystem and Network API
- **Mod Support**: Godot package system and project structure for community content
- Remote play with cross-save functionality using Godot's networking capabilities

### Godot Development Platform
- **Primary Platform**: Godot Engine (version TBD)
- **Export Targets**: Windows, macOS, Linux, Web (WebAssembly), Android, iOS
- **Development Tools**: Godot IDE, GDScript editor, Godot Asset Library
- **Project Structure**: Godot project folder with .godot, project.godot, and res://, src:// directories

## Development Pipeline
- Core gameplay development (Months 1-2)
- Content creation and testing (Months 3-4)
- Final polish and bug fixes (Month 5)
- Release preparation (Month 6)

## Architecture
The game features a modular architecture with Godot's scene-based approach:

### Core Architecture Components
1. **Core Game Engine** - Godot Engine integration and game loop management
2. **World Management System** - Godot scene management and environment loading
3. **Character & Combat System** - Godot Node-based character controller and combat mechanics
4. **Player Progression System** - Attribute management and dynamic class assignment
5. **Magic & Ability System** - Godot spell casting and magical effects
6. **Inventory & Crafting System** - Godot item system and crafting recipes
7. **Dungeon & Difficulty System** - Portal mechanics and rank-based enemy spawning
8. **Quest & Narrative System** - Godot dialogue system and story progression
9. **UI & HUD System** - Godot user interface and heads-up display
10. **Save & Data Management System** - Godot save system and cloud synchronization
11. **Audio & Visual Effects System** - Godot sound design and visual effects
12. **Networking & Multi-Tenancy System** - Godot networking and multiplayer support

### Godot-Specific Architecture Features
- **Scene-Based**: Godot's hierarchical scene management
- **Node-Based**: Godot Node2D and Sprite2D components
- **Resource-Based**: Godot resource system for assets
- **Signal-Based**: GDScript signals for communication
- **Export-Based**: Godot export templates for platforms