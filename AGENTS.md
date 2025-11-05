# STT - OpenCode Development

> Multiple OpenCode development branches and experimental features

## Overview

STT contains several OpenCode development branches focusing on different features, bug fixes, and experimental enhancements for the OpenCode ecosystem.

## Repository Structure

```
stt/
├── opencode                                    # Main OpenCode development
├── opencode_bug-tui-web-token-mismatch     # Bug fix branch
├── opencode_devops-3415-windows-virus-false-positive  # Windows compatibility
├── opencode_err-hacks                        # Error handling improvements
├── opencode-feat-clojure-syntax-highlighting  # Clojure language support
└── .gitmodules                              # Nested submodule configuration
```

## Development Commands

### OpenCode Development
```bash
cd opencode
bun dev                    # Start development server
pnpm build               # Build for production
pnpm test                # Run tests
```

### Feature Branch Development
```bash
cd opencode-feat-clojure-syntax-highlighting
bun dev                    # Develop with Clojure support
pnpm test                # Test syntax highlighting
```

### Bug Fix Branches
```bash
cd opencode_bug-tui-web-token-mismatch
bun dev                    # Test token mismatch fixes
pnpm test                # Verify bug resolution
```

## Cross-Repository Integration

### Related Tools
- **[opencode-openai-codex-auth](../opencode-openai-codex-auth/)**: Plugin development and testing
- **[opencode-hub](../opencode-hub/)**: Package management and distribution
- **[promethean](../promethean/)**: Agent enhancement and orchestration
- **[agent-shell](../agent-shell/)**: Development workflow integration

### 🔗 Comprehensive Cross-References
- **[CROSS_REFERENCES.md](./CROSS_REFERENCES.md)** - Complete cross-references to all related repositories
- **[Workspace AGENTS.md](../AGENTS.md)** - Main workspace documentation
- **[Repository Index](../REPOSITORY_INDEX.md)** - Complete repository overview

### Integration Patterns
1. **Plugin Development**: Use branches for testing opencode-openai-codex-auth
2. **Feature Development**: Isolate experimental features in dedicated branches
3. **Bug Testing**: Separate branches for specific issue resolution
4. **Distribution**: Use opencode-hub for package management

## Branch Specializations

### opencode (main)
- **Purpose**: Primary OpenCode development
- **Focus**: Core functionality and stability
- **Usage**: Main development branch

### opencode-feat-clojure-syntax-highlighting
- **Purpose**: Clojure language support in OpenCode
- **Features**: Syntax highlighting, REPL integration, paredit support
- **Integration**: Works with clojure-mcp for enhanced development

### opencode_bug-tui-web-token-mismatch
- **Purpose**: Fix TUI web token authentication issues
- **Focus**: Authentication flow and token management
- **Related**: Uses patterns from opencode-openai-codex-auth

### opencode_devops-3415-windows-virus-false-positive
- **Purpose**: Windows compatibility and antivirus false positives
- **Focus**: Cross-platform compatibility and security software interaction
- **Integration**: Works with Windows-specific development environments

### opencode_err-hacks
- **Purpose**: Error handling improvements and debugging
- **Focus**: Robust error management and debugging tools
- **Usage**: Development error handling patterns

## Development Workflow

1. **Feature Isolation**: Each feature in dedicated branch
2. **Testing**: Comprehensive testing in branch context
3. **Integration**: Merge with main after validation
4. **Distribution**: Package through opencode-hub

## OpenCode Integration

### Plugin Development
- Use branches for testing new plugin features
- Integrate with opencode-openai-codex-auth patterns
- Test authentication and request flows

### Language Support
- Clojure syntax highlighting branch
- Integration with clojure-mcp for REPL development
- Enhanced editor experience for Clojure developers

### Cross-Platform Compatibility
- Windows-specific bug fixes
- Antivirus software compatibility
- Consistent experience across platforms

## Resources

- [Main OpenCode Repository](https://github.com/sst/opencode)
- [OpenCode Documentation](https://docs.opencode.ai/)
- [Plugin Development](https://github.com/sst/opencode/blob/main/docs/plugins.md)

## Dependencies

- **Bun**: JavaScript runtime and package manager
- **TypeScript**: Type-safe development
- **React**: UI framework (for applicable branches)
- **Node.js**: Runtime environment

## Configuration

### Development Environment
```bash
# Install dependencies
bun install

# Development mode
bun dev

# Production build
bun build
```

### Branch Switching
```bash
# Switch to feature branch
git checkout opencode-feat-clojure-syntax-highlighting

# Switch to main development
git checkout opencode
```

## License

Follows OpenCode main repository license

## Contributing

1. **Branch Creation**: Create feature-specific branches
2. **Testing**: Comprehensive testing in branch context
3. **Documentation**: Update branch-specific documentation
4. **Integration**: Prepare for merge with main