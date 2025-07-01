# How to Perform Feature Isolation Analysis Using File-Based Sub-Agent Communication

## Overview
This workflow provides comprehensive analysis for isolating and understanding specific features within complex codebases through specialized sub-agent delegation with persistent file-based communication. Each analysis phase creates detailed documentation ensuring thorough feature understanding and safe modification strategies.

## Complete Feature Isolation Analysis Workflow Prompt

```
I need to perform feature isolation analysis for [FEATURE DESCRIPTION] in [REPOSITORY/CODEBASE]. Store all sub-agent findings in [DOCUMENT_DIRECTORY]. Follow this file-based feature analysis workflow:

**PHASE 0 - FEATURE SCOPE & CONTEXT PREPARATION (Main Agent):**
1. Create document directory structure in [DOCUMENT_DIRECTORY]:
   - /phase_1_discovery/
   - /phase_2_dependency_analysis/
   - /phase_3_isolation_strategy/
   - /phase_4_modification_guidance/
2. Check existing knowledge graph for this codebase and feature-related patterns
3. Analyze the feature to determine:
   - **Feature Type**: UI component, business logic, data processing, API endpoint, system integration
   - **Feature Scope**: Single file, module, component, service, cross-cutting concern
   - **Complexity Level**: Simple isolated feature, integrated feature, core system feature
   - **Modification Intent**: Understanding, debugging, enhancement, removal, refactoring
4. Define analysis objectives and success criteria
5. Create initial todo breakdown using todo_write with analysis phases
6. Create: [DOCUMENT_DIRECTORY]/feature_context.md (documenting feature description, analysis objectives, and scope)

**PHASE 1 - FEATURE DISCOVERY & MAPPING (4 Parallel Sub-Agents):**
7. Deploy FOUR parallel sub-agents simultaneously for comprehensive feature discovery:

   **Code Location Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/feature_context.md
   - Perform: Code discovery - locate all code directly implementing the feature, identify primary files, functions, classes, components
   - Create: [DOCUMENT_DIRECTORY]/phase_1_discovery/code_location_analysis.md (documenting completed code discovery)

   **Data Flow Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/feature_context.md
   - Perform: Data flow analysis - trace data flow through the feature, identify inputs, outputs, transformations, data dependencies
   - Create: [DOCUMENT_DIRECTORY]/phase_1_discovery/data_flow_analysis.md (documenting completed data flow analysis)

   **User Interface Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/feature_context.md
   - Perform: UI/UX analysis - identify user interface elements, user interactions, visual components, frontend integration points
   - Create: [DOCUMENT_DIRECTORY]/phase_1_discovery/user_interface_analysis.md (documenting completed UI analysis)

   **Integration Points Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/feature_context.md
   - Perform: Integration analysis - identify how feature integrates with other systems, external APIs, databases, services
   - Create: [DOCUMENT_DIRECTORY]/phase_1_discovery/integration_points_analysis.md (documenting completed integration analysis)

8. Main Agent: Read all discovery documents, synthesize feature mapping
9. **IF DISCOVERY CONTRADICTIONS FOUND**: Repeat Phase 1 with clarified scope and conflict resolution instructions
10. **CHECKPOINT 1**: If checkpoints enabled, present feature discovery results and mapping

**PHASE 2 - DEPENDENCY ANALYSIS (5 Parallel Sub-Agents):**
11. Deploy FIVE parallel sub-agents for comprehensive dependency analysis:

    **Direct Dependencies Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/code_location_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/data_flow_analysis.md
    - Perform: Direct dependency analysis - identify immediate dependencies (imports, function calls, object references)
    - Create: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/direct_dependencies_analysis.md (documenting completed direct dependency analysis)

    **Transitive Dependencies Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/direct_dependencies_analysis.md (wait for completion)
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/integration_points_analysis.md
    - Perform: Transitive dependency analysis - identify indirect dependencies, dependency chains, deep coupling analysis
    - Create: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/transitive_dependencies_analysis.md (documenting completed transitive analysis)

    **Reverse Dependencies Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/code_location_analysis.md
    - Perform: Reverse dependency analysis - identify what depends on this feature, consumers, dependent features
    - Create: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/reverse_dependencies_analysis.md (documenting completed reverse dependency analysis)

    **Configuration Dependencies Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/integration_points_analysis.md
    - Perform: Configuration dependency analysis - identify configuration files, environment variables, setup requirements
    - Create: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/configuration_dependencies_analysis.md (documenting completed configuration analysis)

    **Runtime Dependencies Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/data_flow_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/integration_points_analysis.md
    - Perform: Runtime dependency analysis - identify runtime requirements, services, databases, external systems needed at runtime
    - Create: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/runtime_dependencies_analysis.md (documenting completed runtime analysis)

12. Main Agent: Read all dependency analysis documents, create comprehensive dependency map
13. **IF DEPENDENCY CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
14. **CHECKPOINT 2**: If checkpoints enabled, review dependency analysis and impact assessment

**PHASE 3 - ISOLATION STRATEGY (3 Parallel Sub-Agents):**
15. Deploy THREE parallel sub-agents for isolation strategy development:

    **Isolation Planning Sub-Agent:**
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_1_discovery/
    - Read: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/direct_dependencies_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/reverse_dependencies_analysis.md
    - Perform: Isolation strategy development - create plan for safely isolating feature, identify isolation boundaries, plan extraction approach
    - Create: [DOCUMENT_DIRECTORY]/phase_3_isolation_strategy/isolation_planning_analysis.md (documenting completed isolation planning)

    **Risk Assessment Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/transitive_dependencies_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/reverse_dependencies_analysis.md
    - Perform: Risk evaluation - assess isolation risks, identify potential breaking changes, plan risk mitigation strategies
    - Create: [DOCUMENT_DIRECTORY]/phase_3_isolation_strategy/risk_assessment_analysis.md (documenting completed risk assessment)

    **Testing Strategy Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/user_interface_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/runtime_dependencies_analysis.md
    - Perform: Testing strategy development - plan comprehensive testing approach for isolated feature, identify test scenarios
    - Create: [DOCUMENT_DIRECTORY]/phase_3_isolation_strategy/testing_strategy_analysis.md (documenting completed testing strategy)

16. Main Agent: Read all isolation strategy documents, validate approach
17. **IF STRATEGY CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
18. **CHECKPOINT 3**: If checkpoints enabled, review isolation strategy before implementation guidance

**PHASE 4 - MODIFICATION GUIDANCE (4 Sequential Sub-Agents):**
19. Deploy FOUR sub-agents sequentially for implementation guidance:

    **Extraction Guidance Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_isolation_strategy/isolation_planning_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/direct_dependencies_analysis.md
    - Perform: Extraction guidance development - provide step-by-step extraction guidance, safe modification procedures
    - Create: [DOCUMENT_DIRECTORY]/phase_4_modification_guidance/extraction_guidance_analysis.md (documenting extraction guidance)

    **Refactoring Guidance Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_4_modification_guidance/extraction_guidance_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_dependency_analysis/configuration_dependencies_analysis.md
    - Perform: Refactoring guidance development - provide refactoring recommendations, code improvement suggestions
    - Create: [DOCUMENT_DIRECTORY]/phase_4_modification_guidance/refactoring_guidance_analysis.md (documenting refactoring guidance)

    **Integration Guidance Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_4_modification_guidance/refactoring_guidance_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_discovery/integration_points_analysis.md
    - Perform: Integration guidance development - provide guidance for re-integrating modified feature, interface specifications
    - Create: [DOCUMENT_DIRECTORY]/phase_4_modification_guidance/integration_guidance_analysis.md (documenting integration guidance)

    **Validation Guidance Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_isolation_strategy/testing_strategy_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_4_modification_guidance/integration_guidance_analysis.md
    - Perform: Validation guidance development - provide comprehensive validation procedures, testing checklists
    - Create: [DOCUMENT_DIRECTORY]/phase_4_modification_guidance/validation_guidance_analysis.md (documenting validation guidance)

20. Main Agent: Read all modification guidance documents, compile comprehensive feature isolation report

**DOCUMENT STRUCTURE REQUIREMENTS:**

Each sub-agent document must include:

"""markdown
# [Domain] Feature Analysis
**Agent:** [Sub-Agent Name]
**Phase:** [Phase Number]
**Timestamp:** [ISO Timestamp]
**Documents Read:** [List of input documents]
**Analysis Focus:** [Specific analysis domain]

## Executive Summary
[Brief overview of feature analysis completed]

## Detailed Analysis Findings
[Comprehensive analysis within feature domain]

## Feature Components Identified
[Specific feature elements discovered]

## Dependencies and Relationships
[Dependencies and connections identified]

## Isolation Considerations
[Factors affecting feature isolation]

## Integration Points
[How findings relate to other analysis domains]

## Modification Implications
[Impact of potential feature modifications]
"""

**FEATURE ANALYSIS SCOPE ISOLATION:**
- **Discovery sub-agents focus only on their discovery domain** without analyzing dependencies or isolation strategies
- **Dependency sub-agents analyze relationships only** without making isolation recommendations
- **Strategy sub-agents develop approaches** without implementing changes
- **Guidance sub-agents provide implementation direction** without modifying code
- **Each sub-agent works within assigned domain** avoiding overlap with other analysis areas

**CONFLICT RESOLUTION PROTOCOL:**
1. Main Agent identifies contradictions between analysis documents
2. Create feature_analysis_conflict_[timestamp].md documenting specific conflicts
3. Re-run affected sub-agents with conflict context and additional guidance
4. Continue workflow with updated documents

**FEATURE COMPLEXITY ADAPTATION:**
- **Simple Features**: Use abbreviated workflow focusing on Phases 1, 3, and 4 with reduced sub-agent deployment
- **Standard Features**: Use full workflow with standard sub-agent delegation as described
- **Complex Features**: Use extended workflow with additional specialized sub-agents for deep analysis

**HUMAN FEEDBACK OPTIONS:**
- **Default**: Fully autonomous execution with comprehensive feature analysis report
- **Add "WITH CHECKPOINTS"**: Pause after each major phase for review and guidance
- **Add "REVIEW DISCOVERY"**: Pause only after Phase 1 to confirm feature mapping
- **Add "REVIEW DEPENDENCIES"**: Pause only after Phase 2 to validate dependency analysis
- **Add "REVIEW STRATEGY"**: Pause only after Phase 3 to approve isolation approach

**FEATURE TO ANALYZE:**
[FEATURE DESCRIPTION] in [REPOSITORY/CODEBASE] using document directory [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW DISCOVERY | REVIEW DEPENDENCIES | REVIEW STRATEGY]

Begin with Phase 0 feature scope preparation and proceed systematically through each analysis phase with validation checkpoints.
```

## Usage Instructions

1. **Replace placeholders** with specific information:
   - `[FEATURE DESCRIPTION]` - Detailed description of the feature to analyze including expected behavior, user-facing elements
   - `[REPOSITORY/CODEBASE]` - Specific repository or codebase containing the feature
   - `[DOCUMENT_DIRECTORY]` - Absolute path where documents should be stored (e.g., "/project/analysis/user-authentication")

2. **Prepare document directory** - Ensure the specified directory exists and is writable

3. **Choose feedback level** by adding optional modifiers for human checkpoints

4. **Define analysis objectives** clearly in the feature context to guide the analysis process

## Key Benefits of File-Based Communication

- **Comprehensive Feature Documentation**: Complete preservation of all feature analysis findings and relationships
- **Dependency Traceability**: Clear documentation of all feature dependencies and their impact
- **Isolation Safety**: Systematic risk assessment and mitigation planning for safe feature modification
- **Knowledge Building**: Feature patterns and isolation techniques captured for future analysis
- **Modification Guidance**: Detailed implementation guidance for safe feature changes
- **Team Understanding**: Shared knowledge of complex feature relationships and interactions

## Document Organization Example

```
/project/analysis/user-authentication/
├── feature_context.md
├── phase_1_discovery/
│   ├── code_location_analysis.md
│   ├── data_flow_analysis.md
│   ├── user_interface_analysis.md
│   └── integration_points_analysis.md
├── phase_2_dependency_analysis/
│   ├── direct_dependencies_analysis.md
│   ├── transitive_dependencies_analysis.md
│   ├── reverse_dependencies_analysis.md
│   ├── configuration_dependencies_analysis.md
│   └── runtime_dependencies_analysis.md
├── phase_3_isolation_strategy/
│   ├── isolation_planning_analysis.md
│   ├── risk_assessment_analysis.md
│   └── testing_strategy_analysis.md
└── phase_4_modification_guidance/
    ├── extraction_guidance_analysis.md
    ├── refactoring_guidance_analysis.md
    ├── integration_guidance_analysis.md
    └── validation_guidance_analysis.md
```

## Feature Analysis Use Cases

**Understanding Complex Features:**
- Legacy code analysis and documentation
- Feature behavior investigation
- Code archaeology and reverse engineering
- System integration understanding

**Safe Feature Modification:**
- Feature enhancement planning
- Bug fix impact assessment
- Refactoring strategy development
- Feature removal planning

**Code Quality Improvement:**
- Dependency reduction strategies
- Coupling analysis and optimization
- Architecture improvement planning
- Technical debt assessment

**Knowledge Transfer:**
- Team onboarding and training
- Feature documentation creation
- System understanding development
- Maintenance planning

## Advanced Analysis Features

- **Multi-Layer Analysis**: Discovery, dependencies, strategy, and guidance in systematic progression
- **Risk Mitigation**: Comprehensive risk assessment and safe modification planning
- **Dependency Mapping**: Complete understanding of feature relationships and interactions
- **Isolation Planning**: Strategic approach to feature extraction and modification
- **Implementation Guidance**: Practical step-by-step guidance for safe feature changes
- **Knowledge Preservation**: Complete analysis documentation for future reference and team learning
