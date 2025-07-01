# How to Resolve Merge Conflicts Using File-Based Sub-Agent Communication

## Overview
This workflow systematically resolves merge conflicts through strategic analysis and careful integration with specialized sub-agent delegation and persistent file-based communication. Each resolution phase creates detailed documentation ensuring comprehensive conflict analysis and safe resolution.

## Complete Merge Conflict Resolution Workflow Prompt

```
I need to resolve merge conflicts for [MERGE DESCRIPTION] in [REPOSITORY/BRANCH]. Store all sub-agent findings in [DOCUMENT_DIRECTORY]. Follow this file-based conflict resolution workflow:

**PHASE 0 - CONFLICT ASSESSMENT & PREPARATION (Main Agent):**
1. Create document directory structure in [DOCUMENT_DIRECTORY]:
   - /phase_1_conflict_analysis/
   - /phase_2_resolution_strategy/
   - /phase_3_implementation/
   - /phase_4_validation/
2. Check existing knowledge graph for this codebase and previous conflict resolution patterns
3. Analyze the merge situation to determine:
   - **Conflict Scope**: File count, line changes, affected components, merge complexity
   - **Conflict Types**: Code conflicts, dependency conflicts, configuration conflicts, data conflicts
   - **Branch Context**: Feature branches, release branches, hotfix merges, long-running branches
   - **Risk Assessment**: Critical systems affected, potential breaking changes, deployment timeline
4. Identify conflicting files and examine conflict markers
5. Create initial todo breakdown using todo_write with resolution phases
6. Create: [DOCUMENT_DIRECTORY]/conflict_context.md (documenting merge context, conflict scope, and risk assessment)

**PHASE 1 - CONFLICT ANALYSIS (4 Parallel Sub-Agents):**
7. Deploy FOUR parallel sub-agents simultaneously for comprehensive conflict analysis:

   **File-Level Conflict Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/conflict_context.md
   - Perform: File conflict analysis - analyze each conflicting file, understand changes from both branches, assess conflict complexity
   - Create: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/file_conflict_analysis.md (documenting completed file-level analysis)

   **Semantic Conflict Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/conflict_context.md
   - Perform: Semantic conflict analysis - identify logical conflicts beyond textual conflicts, analyze functional impact, behavior changes
   - Create: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/semantic_conflict_analysis.md (documenting completed semantic analysis)

   **Dependency Conflict Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/conflict_context.md
   - Perform: Dependency conflict analysis - analyze dependency version conflicts, package.json conflicts, import/export conflicts
   - Create: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/dependency_conflict_analysis.md (documenting completed dependency analysis)

   **Integration Conflict Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/conflict_context.md
   - Perform: Integration conflict analysis - analyze how changes interact across components, identify system-wide conflict implications
   - Create: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/integration_conflict_analysis.md (documenting completed integration analysis)

8. Main Agent: Read all conflict analysis documents, synthesize findings
9. **IF ANALYSIS CONTRADICTIONS FOUND**: Repeat Phase 1 with clarified scope and conflict resolution instructions
10. **CHECKPOINT 1**: If checkpoints enabled, present conflict analysis and resolution approach

**PHASE 2 - RESOLUTION STRATEGY (3 Parallel Sub-Agents):**
11. Deploy THREE parallel sub-agents for resolution strategy development:

    **Resolution Planning Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/file_conflict_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/semantic_conflict_analysis.md
    - Perform: Resolution strategy development - create detailed resolution plan, prioritize conflicts, determine resolution approach for each conflict type
    - Create: [DOCUMENT_DIRECTORY]/phase_2_resolution_strategy/resolution_planning_analysis.md (documenting completed resolution planning)

    **Risk Assessment Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/integration_conflict_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/conflict_context.md
    - Perform: Risk evaluation - assess resolution risks, identify potential breaking changes, plan mitigation strategies
    - Create: [DOCUMENT_DIRECTORY]/phase_2_resolution_strategy/risk_assessment_analysis.md (documenting completed risk assessment)

    **Testing Strategy Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/semantic_conflict_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/integration_conflict_analysis.md
    - Perform: Testing strategy development - plan comprehensive testing approach, identify test scenarios, create validation framework
    - Create: [DOCUMENT_DIRECTORY]/phase_2_resolution_strategy/testing_strategy_analysis.md (documenting completed testing strategy)

12. Main Agent: Read all resolution strategy documents, validate approach
13. **IF STRATEGY CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
14. **CHECKPOINT 2**: If checkpoints enabled, review resolution strategy before implementation

**PHASE 3 - CONFLICT RESOLUTION IMPLEMENTATION (Sequential Sub-Agents):**
15. Deploy sub-agents sequentially for safe conflict resolution:

    **File Resolution Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_resolution_strategy/resolution_planning_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/file_conflict_analysis.md
    - Perform: File conflict resolution - resolve textual conflicts in each file, merge changes safely, preserve intent from both branches
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/file_resolution_analysis.md (documenting completed file resolution)

    **Semantic Resolution Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_implementation/file_resolution_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/semantic_conflict_analysis.md
    - Perform: Semantic conflict resolution - resolve logical conflicts, ensure behavioral consistency, maintain functional integrity
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/semantic_resolution_analysis.md (documenting completed semantic resolution)

    **Dependency Resolution Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_implementation/semantic_resolution_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/dependency_conflict_analysis.md
    - Perform: Dependency conflict resolution - resolve package conflicts, update dependency versions, ensure compatibility
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/dependency_resolution_analysis.md (documenting completed dependency resolution)

    **Integration Resolution Sub-Agent:**
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_3_implementation/
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/integration_conflict_analysis.md
    - Perform: Integration resolution - ensure all components work together, resolve cross-component conflicts, verify system integration
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/integration_resolution_analysis.md (documenting completed integration resolution)

16. Main Agent: Read all implementation documents, track resolution progress, update todos
17. **CHECKPOINT 3**: If checkpoints enabled, review implemented resolutions before validation

**PHASE 4 - VALIDATION & VERIFICATION (3 Sequential Sub-Agents):**
18. Deploy THREE sub-agents sequentially for comprehensive validation:

    **Build Verification Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_implementation/integration_resolution_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_resolution_strategy/testing_strategy_analysis.md
    - Perform: Build validation - verify project builds successfully, run compilation checks, ensure no build errors
    - Create: [DOCUMENT_DIRECTORY]/phase_4_validation/build_verification_analysis.md (documenting build validation results)

    **Test Execution Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_4_validation/build_verification_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_resolution_strategy/testing_strategy_analysis.md
    - Perform: Test execution - run comprehensive test suite, execute conflict-specific tests, validate functionality
    - Create: [DOCUMENT_DIRECTORY]/phase_4_validation/test_execution_analysis.md (documenting test execution results)

    **Integration Validation Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_4_validation/test_execution_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_conflict_analysis/integration_conflict_analysis.md
    - Perform: Integration validation - verify end-to-end functionality, test system integration, validate conflict resolution success
    - Create: [DOCUMENT_DIRECTORY]/phase_4_validation/integration_validation_analysis.md (documenting integration validation results)

19. Main Agent: Read all validation documents, handle any failures, update knowledge graph with conflict resolution patterns

**DOCUMENT STRUCTURE REQUIREMENTS:**

Each sub-agent document must include:
```markdown
# [Domain] Conflict Analysis/Resolution
**Agent:** [Sub-Agent Name]
**Phase:** [Phase Number]
**Timestamp:** [ISO Timestamp]
**Documents Read:** [List of input documents]
**Conflict Focus:** [Specific conflict domain]

## Executive Summary
[Brief overview of conflict work completed]

## Detailed Analysis/Resolution
[Comprehensive analysis or resolution within domain]

## Conflict Details
[Specific conflicts identified or resolved]

## Resolution Actions
[Actions taken to resolve conflicts]

## Risk Assessment
[Risks identified and mitigation strategies]

## Integration Points
[How work relates to other conflict domains]

## Validation Requirements
[Testing and verification needs]
```

**CONFLICT RESOLUTION SCOPE ISOLATION:**
- **Analysis sub-agents focus only on their conflict domain** without attempting resolution
- **Strategy sub-agents develop approaches** without implementing changes
- **Implementation sub-agents resolve conflicts sequentially** to avoid interference
- **Validation sub-agents verify resolution success** without modifying code
- **Each sub-agent works within assigned domain** ignoring conflicts outside their scope
- **Sequential implementation** prevents sub-agents from interfering with each other's changes

**CONFLICT RESOLUTION SAFETY PRINCIPLES:**
- **Never lose code from either branch** unless explicitly intended
- **Preserve functional intent** from both contributing branches
- **Maintain code quality standards** throughout resolution process
- **Ensure backward compatibility** unless breaking changes are intentional
- **Document all resolution decisions** for future reference and learning

**CONFLICT RESOLUTION PROTOCOL:**
1. Main Agent identifies contradictions between analysis documents
2. Create resolution_conflict_[timestamp].md documenting specific conflicts
3. Re-run affected sub-agents with conflict context and additional guidance
4. Continue workflow with updated documents

**HUMAN FEEDBACK OPTIONS:**
- **Default**: Fully autonomous execution with comprehensive resolution documentation
- **Add "WITH CHECKPOINTS"**: Pause after each major phase for review and approval
- **Add "REVIEW ANALYSIS"**: Pause only after Phase 1 to confirm conflict understanding
- **Add "REVIEW STRATEGY"**: Pause only after Phase 2 to approve resolution approach
- **Add "REVIEW IMPLEMENTATION"**: Pause only after Phase 3 to review changes before validation

**MERGE CONFLICTS TO RESOLVE:**
[MERGE DESCRIPTION] in [REPOSITORY/BRANCH] using document directory [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW ANALYSIS | REVIEW STRATEGY | REVIEW IMPLEMENTATION]

Begin with Phase 0 conflict assessment and proceed systematically through each resolution phase with validation checkpoints.
```

## Usage Instructions

1. **Replace placeholders** with specific information:
   - `[MERGE DESCRIPTION]` - Description of merge situation including source/target branches, conflict scope, urgency
   - `[REPOSITORY/BRANCH]` - Specific repository and branches involved in the merge
   - `[DOCUMENT_DIRECTORY]` - Absolute path where documents should be stored (e.g., "/project/merges/feature-auth-main")

2. **Prepare document directory** - Ensure the specified directory exists and is writable

3. **Choose feedback level** by adding optional modifiers for human checkpoints

4. **Ensure Git workspace is ready** with conflicts visible and tools accessible

## Key Benefits of File-Based Communication

- **Complete Conflict Documentation**: Full preservation of conflict analysis and resolution rationale
- **Resolution Traceability**: Clear documentation of why specific resolution approaches were chosen
- **Risk Management**: Systematic risk assessment and mitigation throughout resolution process
- **Knowledge Building**: Conflict patterns and successful resolution strategies captured for future merges
- **Validation Completeness**: Comprehensive testing and verification documentation
- **Team Learning**: Resolution approaches and techniques shared across development team

## Document Organization Example

```
/project/merges/feature-auth-main/
├── conflict_context.md
├── phase_1_conflict_analysis/
│   ├── file_conflict_analysis.md
│   ├── semantic_conflict_analysis.md
│   ├── dependency_conflict_analysis.md
│   └── integration_conflict_analysis.md
├── phase_2_resolution_strategy/
│   ├── resolution_planning_analysis.md
│   ├── risk_assessment_analysis.md
│   └── testing_strategy_analysis.md
├── phase_3_implementation/
│   ├── file_resolution_analysis.md
│   ├── semantic_resolution_analysis.md
│   ├── dependency_resolution_analysis.md
│   └── integration_resolution_analysis.md
└── phase_4_validation/
    ├── build_verification_analysis.md
    ├── test_execution_analysis.md
    └── integration_validation_analysis.md
```

## Conflict Type Examples

**File-Level Conflicts:**
- Line-by-line textual conflicts
- Whitespace and formatting differences
- Comment and documentation conflicts
- Code structure and organization conflicts

**Semantic Conflicts:**
- Function signature changes
- Variable name and scope conflicts
- Logic and algorithm differences
- API contract modifications

**Dependency Conflicts:**
- Package version mismatches
- Library compatibility issues
- Import and export conflicts
- Configuration file differences

**Integration Conflicts:**
- Cross-component interface changes
- Database schema conflicts
- Configuration and environment differences
- Build and deployment conflicts

## Advanced Features

- **Pattern Recognition**: Documents enable identification of recurring conflict patterns
- **Resolution Reuse**: Previous conflict resolutions inform similar future conflicts
- **Risk Mitigation**: Systematic risk assessment prevents dangerous merge resolutions
- **Quality Assurance**: Comprehensive validation ensures safe conflict resolution
- **Team Knowledge**: Conflict resolution techniques and patterns shared across projects
- **Automated Learning**: Successful resolution patterns can inform future automation
