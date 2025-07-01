# Implement Features in Unfamiliar Codebases with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to implement [FEATURE DESCRIPTION] in unfamiliar codebase. Store findings in [DOCUMENT_DIRECTORY]. Follow this file-based implementation workflow:

**PHASE 0 - CONTEXT PREPARATION:**
1. Create directories: /discovery/, /planning/, /implementation/, /verification/
2. Check existing knowledge graph for codebase
3. Create: [DOCUMENT_DIRECTORY]/feature_scope.md

**PHASE 1A - FOUNDATIONAL DISCOVERY (1 Sub-Agent) - New Codebases:**
- Read: feature_scope.md
- Perform: Codebase overview - structure, tech stack, build system, architecture
- Create: /discovery/foundational_analysis.md

**PHASE 1B - TARGETED ANALYSIS (3 Parallel Sub-Agents):**

**Feature Integration Sub-Agent:**
- Read: feature_scope.md, foundational_analysis.md OR existing_knowledge_summary.md
- Perform: Similar features analysis, integration points, patterns
- Create: /discovery/feature_integration_analysis.md

**Testing & Validation Sub-Agent:**
- Read: feature_scope.md, foundational_analysis.md OR existing_knowledge_summary.md
- Perform: Testing frameworks, error handling, validation approaches
- Create: /discovery/testing_validation_analysis.md

**Development Workflow Sub-Agent:**
- Read: feature_scope.md, foundational_analysis.md OR existing_knowledge_summary.md
- Perform: Deployment patterns, environment config, development workflows
- Create: /discovery/development_workflow_analysis.md

**PHASE 2 - PLANNING (1 Sub-Agent):**
- Read: All discovery/ documents
- Perform: Architecture planning, integration approach, implementation strategy
- Create: /planning/architecture_plan.md

**PHASE 3 - PARALLEL IMPLEMENTATION (Multiple Sub-Agents):**

**Frontend Sub-Agent:**
- Read: architecture_plan.md, feature_integration_analysis.md
- Perform: Frontend implementation - components, UI elements, client logic
- Create: /implementation/frontend_implementation.md

**Backend Sub-Agent:**
- Read: architecture_plan.md, feature_integration_analysis.md
- Perform: Backend implementation - API endpoints, server logic, business logic
- Create: /implementation/backend_implementation.md

**Data Layer Sub-Agent:**
- Read: architecture_plan.md, foundational_analysis.md
- Perform: Data implementation - schemas, models, migrations
- Create: /implementation/data_implementation.md

**Configuration Sub-Agent:**
- Read: architecture_plan.md, development_workflow_analysis.md
- Perform: Configuration implementation - packages, environment, build configs
- Create: /implementation/config_implementation.md

**Integration Sub-Agent:** (Sequential)
- Read: All implementation/ documents
- Perform: Component integration, end-to-end functionality
- Create: /implementation/integration_implementation.md

**Testing Sub-Agent:** (Sequential)
- Read: testing_validation_analysis.md, integration_implementation.md
- Perform: Test implementation following established patterns
- Create: /implementation/testing_implementation.md

**PHASE 4 - VERIFICATION (2 Sequential Sub-Agents):**

**Build Verification Sub-Agent:**
- Read: development_workflow_analysis.md
- Perform: Full test suite, linting, build verification
- Create: /verification/build_verification.md

**Feature Validation Sub-Agent:**
- Read: integration_implementation.md, build_verification.md
- Perform: End-to-end feature validation, user scenarios
- Create: /verification/feature_validation.md

**Document Template:**

"""markdown
# [Domain] Analysis/Implementation
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Relevant For:** [Next Phase]

## Executive Summary
[Brief overview]

## Detailed Analysis/Implementation
[Comprehensive work]

## Integration Points
[Cross-domain relationships]

## Next Phase Requirements
[Guidance for next phase]

## Issues/Conflicts
[Problems identified]
"""

**Scope Isolation:**
- Implementation sub-agents never run global checks during development
- Each sub-agent works only within assigned domain
- Global validation occurs in Phase 4

**Options:** [FEATURE DESCRIPTION] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW PLANNING | REVIEW IMPLEMENTATION]
```

## Key Benefits
- **Knowledge Preservation**: Complete codebase understanding documented
- **Cumulative Learning**: Each feature builds on detailed documentation
- **Parallel Safety**: Independent work without context interference
- **Implementation Guidance**: Detailed documentation for successful delivery
