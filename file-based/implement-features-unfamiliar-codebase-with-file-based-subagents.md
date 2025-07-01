# How to Implement Features in Unfamiliar Codebases Using File-Based Sub-Agent Communication

## Overview
This workflow maximizes efficiency and reliability when implementing new features in unknown codebases by using strategic sub-agent delegation with persistent file-based communication. Each sub-agent documents their findings, enabling precise knowledge transfer and reusable insights.

## Complete Workflow Prompt

```
I need to implement [FEATURE DESCRIPTION] in this unfamiliar codebase. Store all sub-agent findings in [DOCUMENT_DIRECTORY]. Follow this file-based communication workflow:

**PHASE 0 - ENHANCED CONTEXT PREPARATION (Main Agent):**
1. Create document directory structure in [DOCUMENT_DIRECTORY]:
   - /phase_1_discovery/
   - /phase_2_planning/
   - /phase_3_implementation/
   - /phase_4_verification/
2. Check existing knowledge graph for this codebase
3. **IF SUBSTANTIAL KNOWLEDGE EXISTS:**
   - Review stored architecture, patterns, and conventions
   - Create targeted discovery plan focusing only on unknown areas
   - Create: [DOCUMENT_DIRECTORY]/existing_knowledge_summary.md
   - Proceed with abbreviated discovery (Phase 1B)
4. **IF MINIMAL KNOWLEDGE EXISTS:**
   - Proceed with full discovery workflow (Phase 1A)
5. Create initial todo breakdown using todo_write
6. Create: [DOCUMENT_DIRECTORY]/feature_scope.md (documenting feature requirements and initial context)

**PHASE 1A - FOUNDATIONAL DISCOVERY (Single Sub-Agent) - For New Codebases:**
7. Deploy ONE sub-agent for foundational analysis:
   - Read: [DOCUMENT_DIRECTORY]/feature_scope.md
   - Perform: Comprehensive codebase overview - analyze project structure, tech stack, build system, main entry points, core configuration files, overall architectural patterns
   - Create: [DOCUMENT_DIRECTORY]/phase_1_discovery/foundational_analysis.md (documenting completed foundational analysis)

**PHASE 1B - TARGETED ANALYSIS (3 Parallel Sub-Agents):**
8. Deploy THREE parallel sub-agents simultaneously:

   **Feature Integration Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/feature_scope.md
   - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/foundational_analysis.md (if exists) OR [DOCUMENT_DIRECTORY]/existing_knowledge_summary.md
   - Perform: Feature integration analysis - examine similar features, identify integration points, analyze patterns relevant to target feature
   - Create: [DOCUMENT_DIRECTORY]/phase_1_discovery/feature_integration_analysis.md (documenting completed integration analysis)

   **Testing & Validation Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/feature_scope.md
   - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/foundational_analysis.md (if exists) OR [DOCUMENT_DIRECTORY]/existing_knowledge_summary.md
   - Perform: Testing framework analysis - examine testing frameworks, error handling patterns, validation approaches, quality assurance practices
   - Create: [DOCUMENT_DIRECTORY]/phase_1_discovery/testing_validation_analysis.md (documenting completed testing analysis)

   **Development Workflow Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/feature_scope.md
   - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/foundational_analysis.md (if exists) OR [DOCUMENT_DIRECTORY]/existing_knowledge_summary.md
   - Perform: Development workflow analysis - examine deployment patterns, environment configuration, development workflows, build processes
   - Create: [DOCUMENT_DIRECTORY]/phase_1_discovery/development_workflow_analysis.md (documenting completed workflow analysis)

9. Main Agent: Read all discovery documents, check for contradictions, merge with existing knowledge
10. **IF CONTRADICTIONS FOUND**: Repeat Phase 1B with clarified scope and conflict resolution instructions
11. **CHECKPOINT 1**: If checkpoints enabled, summarize codebase findings and confirm approach

**PHASE 2 - SYNTHESIS & PLANNING (Main Agent + 1 Sub-Agent):**
12. Main Agent: Synthesize discoveries, update todos with specific implementation tasks
13. Deploy ONE sub-agent for architecture planning:
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_1_discovery/
    - Perform: Architecture planning - create integration approach, design component relationships, plan implementation strategy
    - Create: [DOCUMENT_DIRECTORY]/phase_2_planning/architecture_plan.md (documenting completed planning analysis)
14. Main Agent: Review architecture plan, create dependency-ordered implementation strategy
15. **CHECKPOINT 2**: If checkpoints enabled, present implementation plan and architecture for approval

**PHASE 3 - PARALLEL IMPLEMENTATION (Multiple Sub-Agents):**
16. Deploy independent sub-agents in parallel:

    **Frontend Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_planning/architecture_plan.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/feature_integration_analysis.md
    - Perform: Frontend implementation - develop frontend components, user interface elements, client-side logic
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/frontend_implementation.md (documenting completed frontend work)

    **Backend Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_planning/architecture_plan.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/feature_integration_analysis.md
    - Perform: Backend implementation - develop API endpoints, server logic, business logic components
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/backend_implementation.md (documenting completed backend work)

    **Data Layer Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_planning/architecture_plan.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/foundational_analysis.md
    - Perform: Data layer implementation - create database schemas, data models, migration scripts
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/data_implementation.md (documenting completed data work)

    **Configuration Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_planning/architecture_plan.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/development_workflow_analysis.md
    - Perform: Configuration implementation - update package files, environment configs, build configurations
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/config_implementation.md (documenting completed config work)

17. Deploy dependent sub-agents sequentially:

    **Integration Sub-Agent:**
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_3_implementation/
    - Perform: Component integration - connect frontend, backend, data components, ensure end-to-end functionality
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/integration_implementation.md (documenting completed integration work)

    **Testing Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/testing_validation_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_implementation/integration_implementation.md
    - Perform: Test implementation - create comprehensive tests following established patterns, ensure feature coverage
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/testing_implementation.md (documenting completed testing work)

18. Main Agent: Track progress, update existing knowledge graph with new observations, update todos as completed
19. **CHECKPOINT 3**: If checkpoints enabled, summarize implementation and confirm testing approach

**PHASE 4 - VERIFICATION & RECOVERY (Sequential Sub-Agents):**
20. Deploy TWO sub-agents sequentially:

    **Build Verification Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/development_workflow_analysis.md
    - Perform: Build verification - run full test suite, linting, build verification, ensure all checks pass
    - Create: [DOCUMENT_DIRECTORY]/phase_4_verification/build_verification.md (documenting verification results)

    **Feature Validation Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_implementation/integration_implementation.md
    - Read: [DOCUMENT_DIRECTORY]/phase_4_verification/build_verification.md
    - Perform: Feature validation - validate feature works end-to-end, test user scenarios, confirm requirements met
    - Create: [DOCUMENT_DIRECTORY]/phase_4_verification/feature_validation.md (documenting validation results)

21. Main Agent: Handle any failures with rollback strategy, final knowledge graph updates and enhancements

**DOCUMENT STRUCTURE REQUIREMENTS:**

Each sub-agent document must include:

"""markdown
# [Domain] Analysis/Implementation
**Agent:** [Sub-Agent Name]
**Phase:** [Phase Number]
**Timestamp:** [ISO Timestamp]
**Documents Read:** [List of input documents]
**Relevant For Next Phase:** [List of domains/agents that should read this]

## Executive Summary
[Brief overview of work completed]

## Detailed Findings/Implementation
[Comprehensive analysis or implementation details]

## Integration Points
[How findings/work relate to other domains]

## Next Phase Requirements
[What subsequent phases need to know]

## Issues/Conflicts
[Any problems or contradictions identified]
"""

**FEATURE IMPLEMENTATION SCOPE ISOLATION:**
- **Implementation sub-agents never run global checks** during development phase
- **Each sub-agent only works within their assigned domain** and ignores errors outside their scope
- **Domain boundaries**: Frontend (components, styles), Backend (API, server logic), Data (models, migrations), Config (package files)
- **File-specific validation only** during implementation - global validation occurs in Phase 4
- **Integration sub-agent** connects components only after all parallel agents complete

**CONFLICT RESOLUTION PROTOCOL:**
1. Main Agent identifies contradictions between documents
2. Create conflict_resolution_[timestamp].md documenting specific conflicts
3. Re-run affected sub-agents with conflict context and additional guidance
4. Continue workflow with updated documents

**HUMAN FEEDBACK OPTIONS:**
- **Default**: Fully autonomous execution with final summary
- **Add "WITH CHECKPOINTS"**: Pause after each major phase for review and approval
- **Add "REVIEW PLANNING"**: Pause only after Phase 2 for architectural approval before implementation
- **Add "REVIEW IMPLEMENTATION"**: Pause only after Phase 3 to review changes before testing

**FEATURE TO IMPLEMENT:**
[FEATURE DESCRIPTION] using document directory [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW PLANNING | REVIEW IMPLEMENTATION]

Begin with Phase 0 and proceed systematically through each phase with proper validation checkpoints.
```

## Usage Instructions

1. **Replace placeholders** with specific information:
   - `[FEATURE DESCRIPTION]` - Detailed description of the feature you want to implement
   - `[DOCUMENT_DIRECTORY]` - Absolute path where documents should be stored (e.g., "/project/features/user-auth")

2. **Prepare document directory** - Ensure the specified directory exists and is writable

3. **Choose feedback level** by adding optional modifiers for human checkpoints

4. **For subsequent features** in the same codebase, this workflow will automatically leverage existing knowledge

## Key Benefits of File-Based Communication

- **Complete Knowledge Preservation**: No information loss through summarization
- **Cumulative Learning**: Each feature builds upon detailed architectural documentation
- **Parallel Safety**: Sub-agents work independently without context interference
- **Selective Context Loading**: Agents only read documents relevant to their domain
- **Persistent Insights**: Documents remain available for future feature development
- **Conflict Detection**: Systematic comparison reveals contradictions and gaps
- **Audit Trail**: Complete record of discovery, planning, and implementation decisions

## Document Organization Example

```
/project/features/user-auth/
├── feature_scope.md
├── existing_knowledge_summary.md (if applicable)
├── phase_1_discovery/
│   ├── foundational_analysis.md
│   ├── feature_integration_analysis.md
│   ├── testing_validation_analysis.md
│   └── development_workflow_analysis.md
├── phase_2_planning/
│   └── architecture_plan.md
├── phase_3_implementation/
│   ├── frontend_implementation.md
│   ├── backend_implementation.md
│   ├── data_implementation.md
│   ├── config_implementation.md
│   ├── integration_implementation.md
│   └── testing_implementation.md
└── phase_4_verification/
    ├── build_verification.md
    └── feature_validation.md
```

## Knowledge Enhancement Benefits

- **Architectural Understanding**: Persistent documentation of codebase patterns and conventions
- **Implementation Patterns**: Reusable approaches for similar features
- **Testing Strategies**: Documented testing patterns for consistent quality
- **Integration Points**: Clear understanding of how components connect
- **Development Workflow**: Captured build, deployment, and development processes

## Common Pitfalls Avoided

- **Information Loss**: Complete findings preserved in structured documents
- **Context Interference**: Sub-agents work with clean, targeted document context
- **Discovery Redundancy**: Documented findings prevent re-analyzing known areas
- **Implementation Conflicts**: Clear domain boundaries prevent parallel work interference
- **Knowledge Fragmentation**: Centralized document repository maintains continuity
- **Testing Gaps**: Documented testing patterns ensure comprehensive coverage
