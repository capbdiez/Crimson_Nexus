# AGENTS - CRIMSON NEXUS

## Coding Standards

### General Principles
- **Clean Code**: Write readable, maintainable code with meaningful variable and function names
- **Consistent Style**: Follow established coding conventions throughout the project
- **Error Handling**: Implement robust error handling with meaningful messages
- **Performance**: Optimize for speed and memory usage
- **Documentation**: Include comprehensive comments and docstrings

### Language-Specific Standards
**C++/C#** (reference only)
- Use consistent brace placement and indentation
- Prefer RAII for resource management
- Use smart pointers where appropriate
- Implement proper copy/move semantics

**GDScript (Primary Development Language)**
- Use const and var appropriately
- Follow GDScript naming conventions (snake_case)
- Implement proper GDScript features (signals, resources, scenes)
- Use @onready and @onready for node initialization
- Leverage Godot's built-in GDScript optimizations

**Godot Engine Standards**
- Follow Godot's scene hierarchy best practices
- Proper use of Node2D, Sprite2D, and other Godot nodes
- Resource management with Godot's resource system
- Animation management with Godot AnimationPlayer

### Code Review
- Peer reviews for all production code changes
- Focus on code quality, security, and performance
- Document decisions and reasoning
- Maintain coding standard compliance

## Documentation Rules

### Technical Documentation
- **API Documentation**: Document all public interfaces with parameter descriptions
- **Architecture Documentation**: Keep architectural decisions current and accessible
- **Code Comments**: Explain complex logic and non-obvious implementations
- **README Files**: Provide clear project overviews and setup instructions

### User Documentation
- **In-Game Tutorials**: Clear, concise guidance for game mechanics
- **Help Menus**: Contextual help and tutorial sections
- **User Guides**: Comprehensive documentation for all features
- **Quick Reference**: Summary sheets for common operations

### Documentation Standards
- Use clear, concise language
- Include code examples where appropriate
- Maintain consistent formatting and structure
- Update documentation with code changes

## Testing Requirements

### Test Coverage
- **Unit Tests**: Minimum 70% coverage for core systems
- **Integration Tests**: All major system interactions tested
- **End-to-End Tests**: Complete user workflows validated
- **Performance Tests**: All systems tested under load

### Test Strategy
- **Automated Testing**: Continuous integration with automated tests
- **Manual Testing**: Human verification of user experience
- **Beta Testing**: Real-world user feedback collection
- **Regression Testing**: Ensure no functionality is broken

### New System Testing (Dungeon & Difficulty System)
- **Unit Tests**: Rank system validation, portal mechanics, wave spawning
- **Integration Tests**: Player progression with dungeon scaling, experience calculations
- **End-to-End Tests**: Complete dungeon runs from portal to boss defeat
- **Stress Tests**: Red portal extreme difficulty scenarios and failure conditions

### Godot-Specific Standards
**Scene System Standards**
- Follow Godot's scene hierarchy best practices
- Proper use of Node2D, Sprite2D, and other Godot nodes
- Resource management with Godot's resource system
- Animation management with Godot AnimationPlayer

**GDScript Standards**
- Use @onready and @onready for node references
- Implement proper GDScript signals for communication
- Leverage Godot's built-in methods and properties
- Optimize GDScript performance with local variables

### Godot Testing Strategy
**Godot Unit Testing**
- Automated testing with Godot Unit Test framework
- Scene-based testing for UI and gameplay
- Performance testing with Godot's built-in profiler
- Integration testing for GDScript and native modules

**Manual Testing**
- Human verification of user experience
- Godot-specific testing for touch controls
- Cross-platform testing for desktop/mobile
- Web browser compatibility testing

### Testing Standards
- Write testable code with clear interfaces
- Mock external dependencies for isolated testing
- Use consistent test naming and organization
- Document test cases and expected outcomes

## Godot Development Pipeline

### Package Management
- npm/yarn dependency management for Godot modules
- Godot Asset Library integration
- Version control with GitHub Actions for CI/CD

### Build Tools
- Godot Engine command-line build system
- Texture compression and optimization tools
- Export templates for multiple platforms
- Automated build scripts for continuous integration

### Deployment Strategy
- CI/CD pipeline for Godot applications
- Web deployment options (WebAssembly, native)
- Mobile deployment (Android, iOS export)
- Desktop deployment (Windows, macOS, Linux export)

### Performance Optimization
- Godot's built-in performance profiler
- Texture atlas and texture packing
- Animation optimization with Godot AnimationPlayer
- Physics performance tuning with Godot physics engine

## Scope-Control Rules

### Feature Management
- **Feature Triage**: Prioritize features based on value and complexity
- **MVP Definition**: Clear definition of minimum viable product
- **Scope Creep Prevention**: Document and justify all scope changes
- **Feature Gates**: Formal approval process for new features

### Timeline Management
- **Milestone Planning**: Structured timeline with clear deliverables
- **Risk Assessment**: Identify and mitigate project risks
- **Progress Tracking**: Regular status updates and metrics
- **Adjustment Process**: Formal process for timeline adjustments

### Resource Management
- **Team Allocation**: Efficient assignment of team members to features
- **Skill Development**: Continuous improvement of team capabilities
- **Budget Management**: Track resource usage and costs
- **Vendor Management**: Third-party resource coordination

## Architecture Compliance Rules

### Design Principles
- **Modularity**: Systems designed as independent, replaceable components
- **Scalability**: Architecture supports future growth and expansion
- **Maintainability**: Easy to understand, modify, and extend
- **Performance**: Optimized for target platforms and user experience

### Architecture Standards
- **Documentation**: Architecture decisions documented and accessible
- **Review Process**: Architecture changes reviewed by architecture committee
- **Pattern Compliance**: Adherence to established architectural patterns
- **Technology Standards**: Use approved technologies and frameworks

### Implementation Standards
- **Code Quality**: Maintain high standards in all implementations
- **Security**: Implement robust security measures
- **Performance**: Optimize for target platforms
- **Testing**: Comprehensive testing at all levels

## Code Quality Guidelines

### File Organization
- **Directory Structure**: Follow established folder organization
- **File Naming**: Use consistent naming conventions
- **Import Organization**: Group imports logically
- **Version Control**: Follow Git best practices

### Development Practices
- **Version Control**: Use feature branches and pull requests
- **Continuous Integration**: Automated builds and testing
- **Code Review**: Peer review process for all changes
- **Testing**: Comprehensive testing at all levels

### Team Collaboration
- **Communication**: Regular team meetings and updates
- **Knowledge Sharing**: Document and share knowledge
- **Mentoring**: Senior team members mentor junior team members
- **Conflict Resolution**: Professional conflict resolution process

This document provides clear guidelines for development practices, documentation, testing, scope management, and architecture compliance to ensure the successful development of Crimson Nexus.