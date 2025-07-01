# How to Perform Thorough Code Reviews Using File-Based Sub-Agent Communication

## Overview
This workflow provides comprehensive code review coverage by deploying specialized sub-agents that communicate through structured documents. This approach ensures complete information preservation, selective context sharing, and persistent knowledge for complex review processes.

## Complete Code Review Workflow Prompt

```
I need to perform a thorough code review for [CODE CHANGE DESCRIPTION] in [REPOSITORY/BRANCH]. Store all sub-agent findings in [DOCUMENT_DIRECTORY]. Follow this file-based communication workflow:

**PHASE 0 - REVIEW SCOPE ASSESSMENT (Main Agent):**
1. Create document directory structure in [DOCUMENT_DIRECTORY]:
   - /phase_1_domain_analysis/
   - /phase_2_integration_analysis/
   - /phase_3_recommendations/
   - /phase_4_final_report/
2. Analyze the scope, complexity, and impact areas of the code changes
3. Create initial scope document: [DOCUMENT_DIRECTORY]/review_scope.md
4. Create todo breakdown using todo_write
5. Determine review depth needed and critical focus areas

**PHASE 1 - MULTI-DOMAIN ANALYSIS (6 Parallel Sub-Agents):**
6. Deploy SIX parallel sub-agents simultaneously, each following this sequence:

   **Security Review Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/review_scope.md
   - Perform: Comprehensive security analysis - examine code for vulnerabilities, attack vectors, authentication/authorization flaws, input validation issues
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/security_findings.md (documenting completed analysis)

   **Performance Review Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/review_scope.md
   - Perform: Comprehensive performance analysis - evaluate algorithm efficiency, database optimization, resource usage, frontend performance impacts
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/performance_findings.md (documenting completed analysis)

   **Architecture Review Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/review_scope.md
   - Perform: Comprehensive architecture analysis - assess design patterns, maintainability, code organization, dependency management, scalability
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/architecture_findings.md (documenting completed analysis)

   **Testing Review Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/review_scope.md
   - Perform: Comprehensive testing analysis - review test coverage, test quality, edge case handling, integration completeness
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/testing_findings.md (documenting completed analysis)

   **Functionality Review Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/review_scope.md
   - Perform: Comprehensive functionality analysis - verify business logic correctness, requirement fulfillment, user experience impact
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/functionality_findings.md (documenting completed analysis)

   **Documentation Review Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/review_scope.md
   - Perform: Comprehensive documentation analysis - check code comments, documentation completeness, API documentation, clarity
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/documentation_findings.md (documenting completed analysis)

7. Main Agent: Read all domain findings documents, check for contradictions
8. **IF CONTRADICTIONS FOUND**: Repeat Phase 1 with clarified scope and specific conflict resolution instructions
9. **CHECKPOINT 1**: If checkpoints enabled, present domain analysis summary and critical findings

**PHASE 2 - CROSS-DOMAIN IMPACT ANALYSIS (1 Sub-Agent):**
10. Deploy ONE sub-agent for integration analysis:
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/
    - Perform: Cross-domain analysis - analyze interactions between domains, assess overall system impact, identify integration risks and conflicts
    - Create: [DOCUMENT_DIRECTORY]/phase_2_integration_analysis/cross_domain_impact.md (documenting completed integration analysis)

11. Main Agent: Read integration analysis, validate findings
12. **IF CONFLICTS WITH DOMAIN ANALYSIS**: Repeat relevant Phase 1 sub-agents with integration context
13. **CHECKPOINT 2**: If checkpoints enabled, present integrated analysis and impact assessment

**PHASE 3 - RISK ASSESSMENT & RECOMMENDATIONS (3 Parallel Sub-Agents):**
14. Deploy THREE parallel sub-agents for recommendation synthesis:

    **Critical Issues Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/security_findings.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/performance_findings.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_integration_analysis/cross_domain_impact.md
    - Perform: Critical issue analysis - prioritize blocking issues, assess severity, determine merge blockers
    - Create: [DOCUMENT_DIRECTORY]/phase_3_recommendations/critical_issues.md (documenting critical issue analysis)

    **Improvement Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/architecture_findings.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/testing_findings.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/documentation_findings.md
    - Perform: Improvement analysis - identify enhancement opportunities, best practice recommendations, optimization suggestions
    - Create: [DOCUMENT_DIRECTORY]/phase_3_recommendations/improvements.md (documenting improvement analysis)

    **Future Impact Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/architecture_findings.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_integration_analysis/cross_domain_impact.md
    - Perform: Future impact analysis - assess long-term maintainability, technical debt implications, architectural consequences
    - Create: [DOCUMENT_DIRECTORY]/phase_3_recommendations/future_impact.md (documenting future impact analysis)

15. Main Agent: Read all recommendation documents, resolve conflicts
16. **IF RECOMMENDATION CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
17. **CHECKPOINT 3**: If checkpoints enabled, review recommendations before report generation

**PHASE 4 - REVIEW REPORT GENERATION (3 Sequential Sub-Agents):**
18. Deploy THREE sub-agents sequentially for comprehensive reporting:

    **Summary Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_recommendations/critical_issues.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_recommendations/improvements.md
    - Perform: Executive summary creation - synthesize key findings, create overall assessment, highlight critical outcomes
    - Create: [DOCUMENT_DIRECTORY]/phase_4_final_report/executive_summary.md (documenting summary analysis)

    **Action Items Sub-Agent:**
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_3_recommendations/
    - Read: [DOCUMENT_DIRECTORY]/phase_4_final_report/executive_summary.md
    - Perform: Action item generation - create prioritized action list, provide specific developer guidance, organize by priority
    - Create: [DOCUMENT_DIRECTORY]/phase_4_final_report/action_items.md (documenting action item analysis)

    **Knowledge Sub-Agent:**
    - Read: All documents from all phases
    - Perform: Knowledge extraction - identify code review patterns, capture lessons learned, document best practices for future reviews
    - Create: [DOCUMENT_DIRECTORY]/phase_4_final_report/lessons_learned.md (documenting knowledge analysis)

19. Main Agent: Compile final review report from all phase 4 documents

**DOCUMENT STRUCTURE REQUIREMENTS:**

Each sub-agent document must include:
```markdown
# [Domain] Analysis Findings
**Agent:** [Sub-Agent Name]
**Phase:** [Phase Number]
**Timestamp:** [ISO Timestamp]
**Documents Read:** [List of input documents]
**Relevant For Next Phase:** [List of domains/agents that should read this]

## Executive Summary
[Brief overview of key findings]

## Detailed Findings
[Comprehensive analysis within domain]

## Integration Points
[How findings relate to other domains]

## Recommendations
[Domain-specific recommendations]

## Conflicts/Uncertainties
[Any contradictions or unclear areas identified]
```

**CONFLICT RESOLUTION PROTOCOL:**
1. Main Agent identifies contradictions between documents
2. Create conflict_resolution_[timestamp].md documenting specific conflicts
3. Re-run affected sub-agents with conflict context and additional guidance
4. Continue workflow with updated documents

**SCOPE ISOLATION PRINCIPLES:**
- Each domain sub-agent focuses exclusively on their expertise area
- Sub-agents only read documents specified in their instructions
- Integration analysis happens only in designated integration phases
- No sub-agent attempts overall assessment - that's main agent coordination

**HUMAN FEEDBACK OPTIONS:**
- **Default**: Fully autonomous execution with final review report
- **Add "WITH CHECKPOINTS"**: Pause after each major phase for review and guidance
- **Add "REVIEW ANALYSIS"**: Pause only after Phase 1 to confirm domain findings
- **Add "REVIEW RECOMMENDATIONS"**: Pause only after Phase 3 to review recommendations

**CODE CHANGES TO REVIEW:**
[CODE CHANGE DESCRIPTION] in [REPOSITORY/BRANCH] using document directory [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW ANALYSIS | REVIEW RECOMMENDATIONS]

Begin with Phase 0 scope assessment and proceed systematically through each phase with comprehensive document-based communication.
```

## Usage Instructions

1. **Replace placeholders** with specific information:
   - `[CODE CHANGE DESCRIPTION]` - Brief description of what was changed
   - `[REPOSITORY/BRANCH]` - Specific repository and branch/PR being reviewed
   - `[DOCUMENT_DIRECTORY]` - Absolute path where documents should be stored (e.g., "/project/reviews/pr-123")

2. **Prepare document directory** - Ensure the specified directory exists and is writable

3. **Choose feedback level** by adding optional modifiers for human checkpoints

## Key Benefits of File-Based Communication

- **Complete Information Preservation**: No data loss through summarization
- **Selective Context Loading**: Sub-agents only read relevant documents, not everything
- **Persistent Knowledge**: Documents remain available for future reference and workflows
- **Conflict Detection**: Systematic comparison of documents reveals contradictions
- **Audit Trail**: Complete record of analysis and decision-making process
- **Scalable Communication**: File system handles large datasets better than prompt context
- **Parallel Safety**: No risk of sub-agents interfering with each other's context

## Document Organization Example

```
/project/reviews/pr-123/
├── review_scope.md
├── phase_1_domain_analysis/
│   ├── security_findings.md
│   ├── performance_findings.md
│   ├── architecture_findings.md
│   ├── testing_findings.md
│   ├── functionality_findings.md
│   └── documentation_findings.md
├── phase_2_integration_analysis/
│   └── cross_domain_impact.md
├── phase_3_recommendations/
│   ├── critical_issues.md
│   ├── improvements.md
│   └── future_impact.md
└── phase_4_final_report/
    ├── executive_summary.md
    ├── action_items.md
    └── lessons_learned.md
```

## Conflict Resolution Example

**Scenario**: Security findings recommend encryption, but performance findings show encryption causes unacceptable latency.

**Resolution Process**:
1. Main Agent creates `/conflict_resolution_2024-07-01T14-30-00Z.md`
2. Document specifies the conflict and additional context needed
3. Re-run Security and Performance sub-agents with conflict awareness
4. New documents include compromise solutions (e.g., selective encryption, performance optimization)

## Advanced Features

- **Document Dependencies**: Clear specification of which documents each sub-agent should read
- **Incremental Updates**: Ability to update specific documents without re-running entire workflow
- **Cross-Project Learning**: Documents can be referenced in future similar reviews
- **Quality Gates**: Main Agent validates document completeness before proceeding to next phase
