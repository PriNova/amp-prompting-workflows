# Feature Isolation Analysis with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to perform feature isolation analysis for [FEATURE DESCRIPTION] in [REPOSITORY/CODEBASE]. Store findings in [DOCUMENT_DIRECTORY]. Follow this file-based feature analysis workflow:

**PHASE 0 - FEATURE SCOPE:**
1. Create directories: /discovery/, /dependency_analysis/, /isolation_strategy/, /modification_guidance/
2. Analyze feature type, scope, complexity level, modification intent
3. Create: [DOCUMENT_DIRECTORY]/feature_context.md

**PHASE 1 - FEATURE DISCOVERY (4 Parallel Sub-Agents):**

**Code Location Sub-Agent:**
- Read: feature_context.md
- Perform: Code discovery - locate implementation, identify files, functions, classes, components
- Create: /discovery/code_location_analysis.md

**Data Flow Sub-Agent:**
- Read: feature_context.md
- Perform: Data flow tracing - inputs, outputs, transformations, dependencies
- Create: /discovery/data_flow_analysis.md

**User Interface Sub-Agent:**
- Read: feature_context.md
- Perform: UI/UX analysis - interface elements, interactions, visual components
- Create: /discovery/user_interface_analysis.md

**Integration Points Sub-Agent:**
- Read: feature_context.md
- Perform: Integration analysis - system connections, external APIs, databases, services
- Create: /discovery/integration_points_analysis.md

**PHASE 2 - DEPENDENCY ANALYSIS (5 Parallel Sub-Agents):**

**Direct Dependencies Sub-Agent:**
- Read: code_location_analysis.md, data_flow_analysis.md
- Perform: Immediate dependencies - imports, function calls, object references
- Create: /dependency_analysis/direct_dependencies_analysis.md

**Transitive Dependencies Sub-Agent:**
- Read: direct_dependencies_analysis.md, integration_points_analysis.md
- Perform: Indirect dependencies, dependency chains, deep coupling analysis
- Create: /dependency_analysis/transitive_dependencies_analysis.md

**Reverse Dependencies Sub-Agent:**
- Read: code_location_analysis.md
- Perform: What depends on this feature - consumers, dependent features
- Create: /dependency_analysis/reverse_dependencies_analysis.md

**Configuration Dependencies Sub-Agent:**
- Read: integration_points_analysis.md
- Perform: Configuration files, environment variables, setup requirements
- Create: /dependency_analysis/configuration_dependencies_analysis.md

**Runtime Dependencies Sub-Agent:**
- Read: data_flow_analysis.md, integration_points_analysis.md
- Perform: Runtime requirements - services, databases, external systems
- Create: /dependency_analysis/runtime_dependencies_analysis.md

**PHASE 3 - ISOLATION STRATEGY (3 Parallel Sub-Agents):**

**Isolation Planning Sub-Agent:**
- Read: All discovery/ documents, direct_dependencies_analysis.md, reverse_dependencies_analysis.md
- Perform: Isolation strategy - safe extraction plan, boundaries, approach
- Create: /isolation_strategy/isolation_planning_analysis.md

**Risk Assessment Sub-Agent:**
- Read: transitive_dependencies_analysis.md, reverse_dependencies_analysis.md
- Perform: Isolation risks, potential breaking changes, mitigation strategies
- Create: /isolation_strategy/risk_assessment_analysis.md

**Testing Strategy Sub-Agent:**
- Read: user_interface_analysis.md, runtime_dependencies_analysis.md
- Perform: Testing approach for isolated feature, test scenarios
- Create: /isolation_strategy/testing_strategy_analysis.md

**PHASE 4 - MODIFICATION GUIDANCE (4 Sequential Sub-Agents):**

**Extraction Guidance Sub-Agent:**
- Read: isolation_planning_analysis.md, direct_dependencies_analysis.md
- Perform: Step-by-step extraction guidance, safe modification procedures
- Create: /modification_guidance/extraction_guidance_analysis.md

**Refactoring Guidance Sub-Agent:**
- Read: extraction_guidance_analysis.md, configuration_dependencies_analysis.md
- Perform: Refactoring recommendations, code improvement suggestions
- Create: /modification_guidance/refactoring_guidance_analysis.md

**Integration Guidance Sub-Agent:**
- Read: refactoring_guidance_analysis.md, integration_points_analysis.md
- Perform: Re-integration guidance, interface specifications
- Create: /modification_guidance/integration_guidance_analysis.md

**Validation Guidance Sub-Agent:**
- Read: testing_strategy_analysis.md, integration_guidance_analysis.md
- Perform: Comprehensive validation procedures, testing checklists
- Create: /modification_guidance/validation_guidance_analysis.md

**Document Template:**
```markdown
# [Domain] Feature Analysis
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Analysis Focus:** [Domain]

## Executive Summary
[Brief overview]

## Detailed Analysis Findings
[Comprehensive analysis]

## Feature Components Identified
[Specific elements discovered]

## Dependencies and Relationships
[Dependencies and connections]

## Isolation Considerations
[Factors affecting isolation]

## Integration Points
[Cross-domain relationships]

## Modification Implications
[Impact of potential changes]
```

**Feature Complexity Adaptation:**
- Simple Features: Abbreviated workflow focusing on Phases 1, 3, 4
- Standard Features: Full workflow as described
- Complex Features: Extended workflow with additional specialized sub-agents

**Options:** [FEATURE DESCRIPTION] in [REPOSITORY/CODEBASE] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW DISCOVERY | REVIEW DEPENDENCIES | REVIEW STRATEGY]
```

## Key Benefits
- **Comprehensive Feature Documentation**: Complete preservation of feature analysis and relationships
- **Dependency Traceability**: Clear documentation of all feature dependencies and impact
- **Isolation Safety**: Systematic risk assessment for safe feature modification
- **Knowledge Building**: Feature patterns and isolation techniques captured for future analysis
