# ARCHITECTURE - CRIMSON NEXUS

## Major Subsystems

### 1. Core Game Engine (Godot Implementation)
| **Purpose**: Main gameplay loop, physics simulation, rendering pipeline
| **Ownership**: Game Systems Team
| **Public Interfaces**: GameState, PhysicsEngine, RenderPipeline
| **Private Components**: GameLoop, SceneSystem, ResourceManager

### 2. World Management System
| **Purpose**: Open world navigation, environment loading, spatial partitioning
| **Ownership**: World Design Team
| **Public Interfaces**: WorldManager, AreaLoader, NavigationSystem
| **Private Components**: TerrainManager, WeatherSystem, TimeSystem

### 3. Character & Combat System
| **Purpose**: Player control, AI behavior, combat mechanics, animations, resource management, skill system
| **Ownership**: Combat Systems Team
| **Public Interfaces**: PlayerController, CombatSystem, AIBrain, ResourceSystem, SkillSystem
| **Private Components**: AnimationController, DamageCalculator, StatusEffectSystem, AdaptiveCombatManager, HybridScalingCalculator

#### Adaptive Combat
- **Pacing Variations**: Fast, frantic hack-and-slash combat against hordes/small bosses vs. slow, tactical combat against giant bosses
- **Combat Modes**: Automatic detection and switching based on enemy composition and player state
- **Dynamic Adjustments**: Real-time scaling of attack speed, defense, and positioning based on combat context

#### Resource Management
- **Physical Classes**: Use 'Energy' resource that depletes slowly during sustained combat
- **Magical Classes**: Use 'Mana' resource with large pool but expensive spell costs
- **Resource Regeneration**: Automatic recovery based on class type and combat state
- **Resource Visualization**: HUD display showing current/max resource levels and regeneration status

#### Skill System
- **5-Skill Slots**: Players can equip exactly 5 active skills at any time
- **Class Integration**: Skills available based on unlocked character classes
- **Skill Swapping**: Dynamic skill management during gameplay
- **Skill Trees**: Progression through skill hierarchies based on character development

#### Hybrid Scaling
- **Mathematical Scaling**: All skill effectiveness scales based on exact class percentages
- **Damage Modifiers**: Physical, magical, and hybrid damage calculations based on mastery
- **Duration Scaling**: Effect durations adjusted according to class specialization
- **Resource Cost Scaling**: Higher costs for spells/skills outside primary class mastery
- **Example Mechanics**: 5% Mage attempting ultimate spell drains all energy due to lack of mastery

### 4. Player Progression System
| **Purpose**: Attribute progression, dynamic class assignment, stat management, skill system integration
| **Ownership**: Progression Systems Team
| **Public Interfaces**: ProgressionSystem, ClassAssigner, StatCalculator
| **Private Components**: AttributeManager, ClassAnalyzer, SkillTreeManager

### 5. Magic & Ability System
| **Purpose**: Spellcasting, magical effects, mana management, visualization
| **Ownership**: Magic Systems Team
| **Public Interfaces**: MagicSystem, SpellManager, EffectRenderer
| **Private Components**: Elementals, ManaPool, ParticleSystemController

### 6. Inventory & Crafting System
| **Purpose**: Item management, crafting recipes, equipment, trading
| **Ownership**: Progression Systems Team
| **Public Interfaces**: InventoryManager, CraftSystem, EquipmentSystem
| **Private Components**: ItemDatabase, RecipeManager, CurrencySystem

### 7. Dungeon & Difficulty System
| **Purpose**: Portal mechanics, rank-based enemy spawning, difficulty scaling, dungeon progression
| **Ownership**: Combat Systems Team
| **Public Interfaces**: PortalSystem, DungeonManager, RankSystem
| **Private Components**: WaveSpawner, EnemyScaler, PortalMutator

### 8. Quest & Narrative System
| **Purpose**: Quest tracking, dialogue, story progression, branching narratives
| **Ownership**: Narrative Team
| **Public Interfaces**: QuestManager, DialogueSystem, StoryEngine
| **Private Components**: QuestGraph, DialogueDatabase, CutsceneSystem

### 9. UI & HUD System
| **Purpose**: User interface, menus, HUD elements, user input handling
| **Ownership**: UX/UI Team
| **Public Interfaces**: UIManager, HUDController, MenuSystem
| **Private Components**: ScreenFade, NotificationSystem, TooltipManager

### 10. Save & Data Management System
| **Purpose**: Game save/load, cloud synchronization, player data persistence
| **Ownership**: Data Management Team
| **Public Interfaces**: SaveSystem, CloudSync, DataValidator
| **Private Components**: ChecksumManager, CompressionEngine, EncryptionLayer

### 11. Audio & Visual Effects System
| **Purpose**: Sound design, music management, particle effects, visual assets
| **Ownership**: Audio/Visual Team
| **Public Interfaces**: AudioSystem, MusicController, VFXManager
| **Private Components**: SoundDatabase, MusicPlaylist, ParticleEngine

### 12. Networking & Multi-Tenancy System
| **Purpose**: Online features, multiplayer support, server communication
| **Ownership**: Network Engineering Team
| **Public Interfaces**: NetworkManager, LobbySystem, Matchmaker
| **Private Components**: PacketHandler, ConnectionManager, SecurityLayer

### Godot-Specific Implementation Features

#### Scene System
| **Purpose**: Hierarchical scene management and organization
| **Ownership**: Scene Management Team
| **Public Interfaces**: SceneTree, ResourceLoader, SceneInstancer
| **Private Components**: AnimationPlayer, MeshInstance, CollisionShape

#### Node System
| **Purpose**: Game object hierarchy and component system
| **Ownership**: Core Systems Team
| **Public Interfaces**: Node2D, Sprite2D, CollisionObject2D
| **Private Components**: AnimatedSprite, TileMap, ParallaxBackground

#### Resource Management
| **Purpose**: Asset loading, management, and optimization
| **Ownership**: Resource Management Team
| **Public Interfaces**: ResourceLoader, DynamicFont, StreamTexture
| **Private Components**: TexturePacker, AnimationLibrary, AudioStream

## Ownership Boundaries

### Team-Owned Systems
| - **Game Systems Team**: Core gameplay, physics, rendering
| - **World Design Team**: Environment, terrain, weather
| - **Combat Systems Team**: Player control, AI, animations, dungeon & difficulty systems
| - **Magic Systems Team**: Spells, abilities, magical effects
| - **Progression Systems Team**: Items, crafting, character progression, attribute management, dynamic class assignment
| - **Narrative Team**: Quests, dialogue, story content
| - **UX/UI Team**: Interface, menus, user experience
| - **Data Management Team**: Saves, clouds, player data
| - **Audio/Visual Team**: Sound, music, visual effects
| - **Network Engineering Team**: Online features, multiplayer

### Godot Team Support
| - **Godot Integration Team**: Godot Engine integration and optimization
| - **GDScript Team**: GDScript implementation and performance tuning
| - **Asset Management Team**: Godot resource and asset management
| - **Scene Management Team**: Godot scene system implementation
| - **Export Team**: Godot export templates and platform support