# Resolve Merge Conflicts with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to resolve merge conflicts for [MERGE DESCRIPTION] in [REPOSITORY/BRANCH]. Store findings in [DOCUMENT_DIRECTORY]. Follow this file-based conflict resolution workflow:

**PHASE 0 - CONFLICT ASSESSMENT:**
1. Create directories: /conflict_analysis/, /resolution_strategy/, /implementation/, /validation/
2. Analyze conflict scope, types, branch context, risk assessment
3. Create: [DOCUMENT_DIRECTORY]/conflict_context.md

**PHASE 1 - CONFLICT ANALYSIS (4 Parallel Sub-Agents):**

**File-Level Conflict Sub-Agent:**
- Read: conflict_context.md
- Perform: File conflict analysis, understand changes from both branches, assess complexity
- Create: /conflict_analysis/file_conflict_analysis.md

**Semantic Conflict Sub-Agent:**
- Read: conflict_context.md
- Perform: Logical conflicts beyond textual, functional impact, behavior changes
- Create: /conflict_analysis/semantic_conflict_analysis.md

**Dependency Conflict Sub-Agent:**
- Read: conflict_context.md
- Perform: Dependency version conflicts, package conflicts, import/export conflicts
- Create: /conflict_analysis/dependency_conflict_analysis.md

**Integration Conflict Sub-Agent:**
- Read: conflict_context.md
- Perform: Cross-component interactions, system-wide conflict implications
- Create: /conflict_analysis/integration_conflict_analysis.md

**PHASE 2 - RESOLUTION STRATEGY (3 Parallel Sub-Agents):**

**Resolution Planning Sub-Agent:**
- Read: file_conflict_analysis.md, semantic_conflict_analysis.md
- Perform: Detailed resolution plan, conflict prioritization, approach determination
- Create: /resolution_strategy/resolution_planning_analysis.md

**Risk Assessment Sub-Agent:**
- Read: integration_conflict_analysis.md, conflict_context.md
- Perform: Resolution risks, potential breaking changes, mitigation strategies
- Create: /resolution_strategy/risk_assessment_analysis.md

**Testing Strategy Sub-Agent:**
- Read: semantic_conflict_analysis.md, integration_conflict_analysis.md
- Perform: Testing approach, validation framework, test scenarios
- Create: /resolution_strategy/testing_strategy_analysis.md

**PHASE 3 - IMPLEMENTATION (4 Sequential Sub-Agents):**

**File Resolution Sub-Agent:**
- Read: resolution_planning_analysis.md, file_conflict_analysis.md
- Perform: Textual conflict resolution, safe merging, intent preservation
- Create: /implementation/file_resolution_analysis.md

**Semantic Resolution Sub-Agent:**
- Read: file_resolution_analysis.md, semantic_conflict_analysis.md
- Perform: Logical conflict resolution, behavioral consistency, functional integrity
- Create: /implementation/semantic_resolution_analysis.md

**Dependency Resolution Sub-Agent:**
- Read: semantic_resolution_analysis.md, dependency_conflict_analysis.md
- Perform: Package conflicts, version updates, compatibility assurance
- Create: /implementation/dependency_resolution_analysis.md

**Integration Resolution Sub-Agent:**
- Read: All implementation/ documents, integration_conflict_analysis.md
- Perform: Component integration, cross-component conflicts, system verification
- Create: /implementation/integration_resolution_analysis.md

**PHASE 4 - VALIDATION (3 Sequential Sub-Agents):**

**Build Verification Sub-Agent:**
- Read: integration_resolution_analysis.md, testing_strategy_analysis.md
- Perform: Build validation, compilation checks, build error elimination
- Create: /validation/build_verification_analysis.md

**Test Execution Sub-Agent:**
- Read: build_verification_analysis.md, testing_strategy_analysis.md
- Perform: Comprehensive test suite, conflict-specific tests, functionality validation
- Create: /validation/test_execution_analysis.md

**Integration Validation Sub-Agent:**
- Read: test_execution_analysis.md, integration_conflict_analysis.md
- Perform: End-to-end functionality, system integration, resolution success verification
- Create: /validation/integration_validation_analysis.md

**Document Template:**
```markdown
# [Domain] Conflict Analysis/Resolution
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Conflict Focus:** [Domain]

## Executive Summary
[Brief overview]

## Detailed Analysis/Resolution
[Comprehensive work within domain]

## Conflict Details
[Specific conflicts identified/resolved]

## Resolution Actions
[Actions taken to resolve conflicts]

## Risk Assessment
[Risks and mitigation strategies]

## Integration Points
[Cross-domain relationships]

## Validation Requirements
[Testing and verification needs]
```

**Conflict Resolution Safety:**
- Never lose code from either branch unless explicitly intended
- Preserve functional intent from both contributing branches
- Maintain code quality standards throughout resolution
- Ensure backward compatibility unless breaking changes intentional
- Document all resolution decisions for future reference

**Options:** [MERGE DESCRIPTION] in [REPOSITORY/BRANCH] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW ANALYSIS | REVIEW STRATEGY | REVIEW IMPLEMENTATION]
```

## Key Benefits
- **Complete Conflict Documentation**: Full preservation of conflict analysis and resolution rationale
- **Resolution Traceability**: Clear documentation of resolution approach selection
- **Risk Management**: Systematic risk assessment and mitigation throughout process
- **Knowledge Building**: Conflict patterns and successful resolution strategies captured
