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
- Real-time 60 FPS on modern hardware
- **2D Pixel Art Style**: Hand-drawn pixel graphics with nostalgic charm
- Dynamic lighting and atmospheric effects
- Comprehensive accessibility features
- Cloud and local save systems
- Mod support for community content
- Remote play with cross-save functionality

## Development Pipeline
- Core gameplay development (Months 1-2)
- Content creation and testing (Months 3-4)
- Final polish and bug fixes (Month 5)
- Release preparation (Month 6)

## Architecture
The game features a modular architecture with 12 major subsystems:
1. Core Game Engine
2. World Management System
3. Character & Combat System
4. **Player Progression System**
5. Magic & Ability System
6. Inventory & Crafting System
7. Dungeon & Difficulty System
8. Quest & Narrative System
9. UI & HUD System
10. Save & Data Management System
11. Audio & Visual Effects System
12. Networking & Multi-Tenancy System