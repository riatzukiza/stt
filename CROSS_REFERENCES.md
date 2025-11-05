# STT Cross-Reference Documentation

> Multiple OpenCode development branches and experimental features with comprehensive repository cross-references

## 🔗 Repository Cross-References

This document provides comprehensive cross-references to all related repositories in the OpenCode development ecosystem, enabling agents to navigate between related tools, dependencies, and integration patterns seamlessly.

### 🏗️ Development Infrastructure Dependencies

#### **Agent Development & Orchestration**
- **[promethean](https://github.com/riatzukiza/promethean)** - Local LLM enhancement system and autonomous agent framework
  - [AGENTS.md](https://github.com/riatzukiza/promethean/blob/main/AGENTS.md)
  - [CROSS_REFERENCES.md](https://github.com/riatzukiza/promethean/blob/main/CROSS_REFERENCES.md)
  - [README.md](https://github.com/riatzukiza/promethean/blob/main/README.md)
  - **Integration**: Use Promethean agents for automated OpenCode testing and enhancement

- **[agent-shell](https://github.com/riatzukiza/agent-shell)** - Emacs-based agent shell for ACP (Agent Client Protocol)
  - [AGENTS.md](https://github.com/riatzukiza/agent-shell/blob/main/AGENTS.md)
  - [README.md](https://github.com/riatzukiza/agent-shell/blob/main/README.org)
  - **Integration**: Interactive development workflow for OpenCode branches

#### **Authentication & Security**
- **[opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth)** - OpenAI Codex OAuth authentication plugin
  - [AGENTS.md](https://github.com/numman-ali/opencode-openai-codex-auth/blob/main/AGENTS.md)
  - [README.md](https://github.com/numman-ali/opencode-openai-codex-auth/blob/main/README.md)
  - **Integration**: Authentication patterns for OpenCode plugin development

### 🔧 Tooling & SDK Dependencies

#### **TypeScript SDK Integration**
- **[moofone/codex-ts-sdk](https://github.com/moofone/codex-ts-sdk)** - TypeScript SDK for OpenAI Codex with cloud tasks
  - [AGENTS.md](https://github.com/moofone/codex-ts-sdk/blob/main/AGENTS.md)
  - [README.md](https://github.com/moofone/codex-ts-sdk/blob/main/README.md)
  - **Integration**: TypeScript-based OpenCode plugin development

#### **Rust-Based Runtime**
- **[openai/codex](https://github.com/openai/codex)** - Rust-based Codex CLI and runtime
  - [AGENTS.md](https://github.com/openai/codex/blob/main/AGENTS.md)
  - [README.md](https://github.com/openai/codex/blob/main/README.md)
  - **Integration**: High-performance OpenCode components

### 🌐 Web & Frontend Integration

#### **Package Management & Distribution**
- **[opencode-hub](https://github.com/riatzukiza/devel/tree/main/opencode-hub)** - Centralized opencode coordination and distribution
  - [AGENTS.md](https://github.com/riatzukiza/devel/blob/main/opencode-hub/AGENTS.md)
  - [README.md](https://github.com/riatzukiza/devel/blob/main/opencode-hub/README.md)
  - **Integration**: Package distribution for STT branches

#### **Full-Stack Applications**
- **[riatzukiza/openhax](https://github.com/riatzukiza/openhax)** - Full-stack application with Reactant + Fastify
  - [AGENTS.md](https://github.com/riatzukiza/openhax/blob/main/AGENTS.md)
  - **Integration**: Full-stack patterns for OpenCode web interfaces

### ⚙️ Configuration & Environment

#### **System Configuration**
- **[dotfiles](https://github.com/riatzukiza/devel/tree/main/dotfiles)** - System configuration and environment setup
  - [AGENTS.md](https://github.com/riatzukiza/devel/blob/main/dotfiles/.config/opencode/AGENTS.md)
  - **Integration**: Development environment setup for OpenCode branches

## 🔄 Branch-Specific Integration Patterns

### **opencode (main branch)**
#### **Core Dependencies**
- **Authentication**: [opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth) for OAuth flows
- **Agent Testing**: [promethean](https://github.com/riatzukiza/promethean) for automated testing
- **Development**: [agent-shell](https://github.com/riatzukiza/agent-shell) for interactive development

#### **Integration Commands**
```bash
# Test with authentication plugin
cd ../opencode-openai-codex-auth && pnpm build && cp dist/* ../stt/opencode/plugins/

# Agent-based testing
cd ../promethean && pnpm --filter @promethean-os/agent test

# Interactive development
cd ../agent-shell && emacs agent-shell.el
```

### **opencode-feat-clojure-syntax-highlighting**
#### **Clojure Ecosystem Integration**
- **[clojure-mcp](https://github.com/bhauman/clojure-mcp)** - MCP server for Clojure REPL-driven development
  - [AGENTS.md](https://github.com/bhauman/clojure-mcp/blob/main/AGENTS.md)
  - [README.md](https://github.com/bhauman/clojure-mcp/blob/main/README.md)
  - **Integration**: REPL integration for Clojure syntax highlighting

#### **Clojure Development Workflow**
```bash
# Clojure MCP integration
cd ../clojure-mcp && pnpm install && pnpm test

# Test syntax highlighting
cd opencode-feat-clojure-syntax-highlighting
bun dev  # with Clojure files for testing
```

### **opencode_bug-tui-web-token-mismatch**
#### **Authentication Focus**
- **Primary**: [opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth) for token management
- **Testing**: [promethean](https://github.com/riatzukiza/promethean) agents for authentication flow testing
- **Development**: [agent-shell](https://github.com/riatzukiza/agent-shell) for debugging

#### **Token Management Testing**
```bash
# Authentication plugin development
cd ../opencode-openai-codex-auth
pnpm test && pnpm build

# Test token mismatch fixes
cd opencode_bug-tui-web-token-mismatch
bun dev  # with authentication test scenarios
```

### **opencode_devops-3415-windows-virus-false-positive**
#### **Windows Integration**
- **Environment**: [dotfiles](https://github.com/riatzukiza/devel/tree/main/dotfiles) for Windows configuration
- **Build**: [openai/codex](https://github.com/openai/codex) for Windows-compatible binaries
- **Testing**: Cross-platform testing with all branches

#### **Windows Development Setup**
```bash
# Windows environment setup
cd ../dotfiles && ./.setup/windows.sh

# Windows-compatible builds
cd ../openai/codex && cargo build --target x86_64-pc-windows-msvc
```

### **opencode_err-hacks**
#### **Error Handling Integration**
- **Patterns**: All repositories for error handling best practices
- **Testing**: [promethean](https://github.com/riatzukiza/promethean) agents for error scenario testing
- **Documentation**: Cross-repository error handling documentation

## 🔄 Cross-Repository Development Workflows

### **Plugin Development Workflow**
1. **Prototype**: Use STT branches for rapid prototyping
2. **Authenticate**: Integrate [opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth) patterns
3. **Test**: Use [promethean](https://github.com/riatzukiza/promethean) agents for automated testing
4. **Distribute**: Package through [opencode-hub](https://github.com/riatzukiza/devel/tree/main/opencode-hub)

### **Feature Development Workflow**
1. **Branch Creation**: Isolate features in dedicated STT branches
2. **Integration**: Connect with relevant repositories (clojure-mcp for language features)
3. **Testing**: Cross-repository testing with [agent-shell](https://github.com/riatzukiza/agent-shell)
4. **Documentation**: Update cross-references in all related docs

### **Bug Fix Workflow**
1. **Isolation**: Create dedicated bug fix branches
2. **Reproduction**: Use tools from [promethean](https://github.com/riatzukiza/promethean) for bug reproduction
3. **Fix**: Implement and test with cross-repository dependencies
4. **Validation**: Test with all relevant repositories

## 📋 Quick Reference Commands

### **Cross-Repository Development**
```bash
# Full development environment setup
cd ../promethean && pnpm build
cd ../agent-shell && emacs agent-shell.el
cd ../clojure-mcp && pnpm install
cd ../opencode-openai-codex-auth && pnpm build

# STT branch development
cd opencode && bun dev
cd opencode-feat-clojure-syntax-highlighting && bun dev
cd opencode_bug-tui-web-token-mismatch && bun dev
```

### **Integration Testing**
```bash
# Cross-repository testing
cd ../promethean && pnpm --filter @promethean-os/test-runner run --suite stt-integration
cd ../clojure-mcp && pnpm test --integration
cd ../opencode-openai-codex-auth && pnpm test --e2e
```

## 🎯 Decision Trees for Agents

### **Choosing Development Branch**
- **Core OpenCode development?** → `opencode` branch
- **Clojure language support?** → `opencode-feat-clojure-syntax-highlighting` + [clojure-mcp](https://github.com/bhauman/clojure-mcp)
- **Authentication issues?** → `opencode_bug-tui-web-token-mismatch` + [opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth)
- **Windows compatibility?** → `opencode_devops-3415-windows-virus-false-positive` + [dotfiles](https://github.com/riatzukiza/devel/tree/main/dotfiles)
- **Error handling improvements?** → `opencode_err-hacks` + all repositories

### **Integration Complexity**
- **Simple**: Single branch + [opencode-openai-codex-auth](https://github.com/numman-ali/opencode-openai-codex-auth)
- **Medium**: Branch + [promethean](https://github.com/riatzukiza/promethean) + [agent-shell](https://github.com/riatzukiza/agent-shell)
- **Complex**: Multiple branches + full ecosystem integration

## 📚 Additional Documentation

- **[Workspace Documentation](https://github.com/riatzukiza/devel/blob/main/AGENTS.md)** - Main workspace coordination
- **[Repository Index](https://github.com/riatzukiza/devel/blob/main/REPOSITORY_INDEX.md)** - Complete repository overview
- **[Git Submodules Documentation](https://github.com/riatzukiza/devel/blob/main/docs/reports/research/git-submodules-documentation.md)** - Technical submodule details
- **[Promethean Cross-References](https://github.com/riatzukiza/promethean/blob/main/CROSS_REFERENCES.md)** - Agent framework integration

## 🌐 External Resources

- **[Main OpenCode Repository](https://github.com/sst/opencode)** - Upstream OpenCode project
- **[OpenCode Documentation](https://docs.opencode.ai/)** - Official documentation
- **[Plugin Development](https://github.com/sst/opencode/blob/main/docs/plugins.md)** - Plugin development guide

---

## License

Follows OpenCode main repository license