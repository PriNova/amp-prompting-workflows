# File-Based Amp Prompting Workflows

## Overview

This repository contains a comprehensive collection of **file-based sub-agent orchestration workflows** for Amp. These workflows leverage persistent document-based communication between sub-agents to achieve superior reliability, knowledge preservation, and execution efficiency compared to traditional briefing-based approaches.

**Two variants available:**
- **Full workflows** ([file-based/](file-based/)): Comprehensive analysis and documentation for complex projects
- **[Minified workflows](minified/file-based/)**: Streamlined 80-85% shorter versions for smaller codebases

## Why File-Based Communication Works Flawlessly

### 🎯 **Zero Information Loss**
Unlike traditional agent briefing systems where context gets compressed and potentially lost, file-based communication preserves **complete detailed analysis** in structured documents. Each sub-agent reads the full findings from previous phases, ensuring no critical insights are lost in translation.

### 📁 **Persistent Knowledge Graph**
Every analysis, finding, and decision is documented in organized files that:
- **Remain accessible** throughout the entire project lifecycle
- **Build institutional knowledge** for future similar projects
- **Enable knowledge reuse** across different features and codebases
- **Create audit trails** for debugging workflow issues

### 🔄 **Conflict Detection & Resolution**
File-based documentation allows systematic comparison between sub-agent findings, making it easy to:
- **Identify contradictions** between different analyses
- **Resolve conflicts** through document review and synthesis
- **Validate findings** against multiple independent sources
- **Ensure consistency** across all project phases

### ⚡ **Optimized Parallel Execution**
Sub-agents can work **completely independently** without waiting for briefings:
- **No serialization bottlenecks** - all agents can start simultaneously
- **Selective context loading** - agents only read relevant documents
- **Scope isolation** - agents focus purely on their assigned domain
- **Faster overall execution** through true parallel processing

### 🏗️ **Scalable Architecture**
The document-based approach scales seamlessly from simple bug fixes to complex multi-month projects:
- **Modular phase structure** adapts to project complexity
- **Standardized document templates** ensure consistency
- **Flexible agent deployment** based on project needs
- **Checkpoint integration** for human feedback and course correction

## Available Workflows

### 🐛 **Bug Fixing & Debugging**
- **[Fix Bugs in Unfamiliar Codebases](file-based/fix-bugs-unfamiliar-codebase-with-file-based-subagents.md)** - Evidence-based debugging with adaptive investigation strategies

### 🚀 **Feature Development**
- **[Implement Features in Unfamiliar Codebases](file-based/implement-features-unfamiliar-codebase-with-file-based-subagents.md)** - Efficient feature development with knowledge reuse and adaptive discovery

### 📊 **Analysis & Review**
- **[Critical Performance Analysis](file-based/critical-performance-analysis-with-file-based-subagents.md)** - Game engine/graphics engine quality performance analysis
- **[Feature Isolation Analysis](file-based/feature-isolation-analysis-with-file-based-subagents.md)** - Complete feature tracing and dependency analysis  
- **[Thorough Code Review](file-based/thorough-code-review-with-file-based-subagents.md)** - Multi-domain comprehensive review coverage

### 🎯 **Strategic & Business**
- **[Market Demand Analysis](file-based/market-demand-analysis-with-file-based-subagents.md)** - Comprehensive market research and validation
- **[Idea Manifestation](file-based/idea-manifestation-with-file-based-subagents.md)** - Concept to reality using structured IDEA framework
- **[Strategic Goal Planning](file-based/strategic-goal-planning-with-file-based-subagents.md)** - Goal analysis to execution framework

### 🔧 **Development Operations**
- **[Resolve Merge Conflicts](file-based/resolve-merge-conflicts-with-file-based-subagents.md)** - Intent-driven conflict resolution with context preservation

### 🏛️ **Meta-Framework**
- **[Strategic Sub-Agent Orchestration Framework](file-based/strategic-subagent-orchestration-framework-with-file-based-communication.md)** - Unified framework covering all project types with file-based communication

## Key Advantages Over Briefing-Based Systems

| Aspect | File-Based Approach | Traditional Briefing System |
|--------|-------------------|---------------------------|
| **Information Preservation** | ✅ Complete details preserved | ❌ Information loss through summarization |
| **Knowledge Building** | ✅ Persistent, reusable knowledge | ❌ Knowledge disappears after project |
| **Parallel Execution** | ✅ True independent parallel work | ❌ Serial bottlenecks at briefing points |
| **Conflict Detection** | ✅ Systematic document comparison | ❌ Conflicts hidden in compressed briefings |
| **Context Access** | ✅ Selective, complete context loading | ❌ Context depends on briefing quality |
| **Audit Trail** | ✅ Complete decision history | ❌ Limited visibility into reasoning |
| **Debugging Workflows** | ✅ Document review reveals issues | ❌ Difficult to trace workflow problems |
| **Knowledge Transfer** | ✅ Documents transfer between projects | ❌ Knowledge trapped in completed workflows |

## Document Structure Standards

Each workflow follows consistent document organization:

```
[DOCUMENT_DIRECTORY]/
├── phase_1_[domain]/
│   ├── [analysis_type]_analysis.md
│   └── [domain]_findings.md
├── phase_2_[domain]/
│   ├── [design_type]_design.md
│   └── [strategy]_strategy.md
├── phase_3_[domain]/
│   └── [implementation]_plan.md
└── project_summary.md
```

### Document Content Standards
- **Structured Analysis**: Consistent templates for each analysis type
- **Complete Findings**: No summarization - full details preserved
- **Clear Dependencies**: Explicit documentation of inter-phase requirements
- **Decision Rationale**: Full reasoning behind all architectural choices
- **Implementation Guidance**: Specific, actionable recommendations

## Usage Patterns

### 1. **Single Workflow Execution**
```
I need to [fix bug/implement feature/analyze performance] in this codebase. 
Store all sub-agent findings in ./project_docs/. 
Follow the file-based [workflow_name] workflow.
```

### 2. **Multi-Phase Project Management**
```
I need to conduct a comprehensive analysis and implementation project. 
Store findings in ./project_analysis/. 
Start with market analysis, then move to feature implementation.
```

### 3. **Knowledge Building Across Projects**
```
I'm working on a similar codebase to [previous_project]. 
Review documents in ./previous_analysis/ and extend with new findings in ./current_analysis/.
```

## Workflow Variants

### Full File-Based Workflows
The workflows in the [file-based/](file-based/) directory provide **comprehensive, production-ready** orchestration with complete documentation, detailed phase breakdowns, and extensive sub-agent coordination. Best for:
- **Complex codebases** with multiple interconnected systems
- **Large-scale projects** requiring thorough analysis and planning
- **Production environments** where complete documentation is essential
- **Team collaboration** where knowledge transfer is critical

### Minified Versions
For simpler projects, streamlined minified versions are available in the [minified/file-based/](minified/file-based/) directory. These maintain all core functionality while being **80-85% more concise**:

**Preserved Elements:**
- Phase-based structure with sub-agent delegation
- File-based communication system
- Scope isolation principles  
- All critical workflow steps

**Reduced Elements:**
- Detailed examples and verbose explanations
- Extensive briefing templates
- Repetitive content and elaborations

**Ideal for:**
- **Small to medium codebases** (< 50k lines of code)
- **Time-sensitive debugging** and quick feature implementation
- **Solo developers** who prefer concise instructions
- **Familiar codebases** where extensive discovery isn't needed

## Getting Started

1. **Choose Your Workflow Variant**: 
   - Use **[full workflows](file-based/)** for complex/unknown codebases requiring comprehensive analysis
   - Use **[minified workflows](minified/file-based/)** for smaller/familiar codebases needing quick execution
2. **Create Document Directory**: Set up a dedicated directory for storing sub-agent findings  
3. **Execute the Workflow**: Use the complete workflow prompt with your specific project details
4. **Review Documents**: Examine the generated analysis documents for insights and guidance
5. **Build Knowledge Base**: Preserve documents for future similar projects

## Technical Requirements

### Amp CLI Installation

These workflows are designed specifically for **[Amp CLI](https://ampcode.com)**, an agentic coding tool built by Sourcegraph that provides advanced sub-agent orchestration capabilities.

#### Installation Options:

**VS Code Extension:**
1. Sign in to [ampcode.com](https://ampcode.com/settings)
2. Follow the extension installation instructions for VS Code, Cursor, or Windsurf

**Command Line Interface:**
```bash
# Using npm
npm install -g @sourcegraph/amp

# Using pnpm  
pnpm add -g @sourcegraph/amp

# Using yarn
yarn global add @sourcegraph/amp

# Using npx (no installation required)
npx @sourcegraph/amp
```

For complete installation instructions, visit: https://ampcode.com/manual#install

#### System Requirements:
- **File System Access**: Amp must be able to create and read markdown files
- **Directory Structure**: Ability to create organized directory hierarchies  
- **Context Loading**: Support for reading multiple documents as context
- **Sub-Agent Support**: Amp's built-in Task tool for sub-agent orchestration

## Contributing

When creating new workflows or enhancing existing ones:

1. **Follow Document Standards**: Use consistent directory and file naming conventions
2. **Preserve Complete Information**: Avoid summarization in favor of complete analysis preservation  
3. **Enable Parallel Execution**: Design sub-agent tasks to be truly independent
4. **Include Checkpoint Options**: Allow for human feedback integration
5. **Document Knowledge Transfer**: Clearly specify which documents each sub-agent should read

## License

This repository is intended for public use and improvement of AI agent orchestration patterns. Please attribute when using or extending these workflows.

---

*These workflows represent a fundamental shift from ephemeral briefing-based communication to persistent document-based knowledge systems, unlocking new levels of reliability and efficiency in AI-assisted software development.*
