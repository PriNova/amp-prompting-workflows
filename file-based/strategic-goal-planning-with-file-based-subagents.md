# How to Create Strategic Goal Planning Using File-Based Sub-Agent Communication

## Overview
This workflow systematically creates comprehensive strategic plans for achieving complex goals through specialized sub-agent delegation with persistent file-based communication. Each planning phase creates detailed documentation ensuring thorough analysis and actionable implementation strategies.

## Complete Strategic Goal Planning Workflow Prompt

```
I need to create strategic plan for [GOAL DESCRIPTION]. Store all sub-agent findings in [DOCUMENT_DIRECTORY]. Follow this file-based strategic planning workflow:

**PHASE 0 - GOAL CONTEXT & PREPARATION (Main Agent):**
1. Create document directory structure in [DOCUMENT_DIRECTORY]:
   - /phase_1_analysis/
   - /phase_2_solution_architecture/
   - /phase_3_detailed_planning/
   - /phase_4_execution_framework/
2. Check existing knowledge graph for related projects, patterns, and methodologies
3. Analyze the goal to determine:
   - **Goal Category**: Business objective, technical implementation, organizational transformation, process improvement
   - **Scope Level**: Individual, team, department, organization, market
   - **Complexity Indicators**: Simple (< 3 months), medium (3-12 months), complex (12+ months)
   - **Resource Implications**: Budget, timeline, skills, infrastructure, stakeholder involvement
4. Define success criteria and key performance indicators
5. Create initial todo breakdown using todo_write with planning phases
6. Create: [DOCUMENT_DIRECTORY]/goal_context.md (documenting goal vision, scope, and requirements)

**PHASE 1A - FOUNDATIONAL ANALYSIS (4 Parallel Sub-Agents):**
7. Deploy FOUR parallel sub-agents simultaneously:

   **Context Analysis Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/goal_context.md
   - Perform: Context assessment - analyze current state, existing systems, stakeholders, environment factors, baseline conditions
   - Create: [DOCUMENT_DIRECTORY]/phase_1_analysis/context_analysis.md (documenting completed context assessment)

   **Requirements Analysis Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/goal_context.md
   - Perform: Requirements definition - define detailed requirements, constraints, dependencies, success metrics, acceptance criteria
   - Create: [DOCUMENT_DIRECTORY]/phase_1_analysis/requirements_analysis.md (documenting completed requirements definition)

   **Feasibility Analysis Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/goal_context.md
   - Perform: Feasibility assessment - assess technical feasibility, resource availability, timeline viability, potential blockers
   - Create: [DOCUMENT_DIRECTORY]/phase_1_analysis/feasibility_analysis.md (documenting completed feasibility assessment)

   **Risk Analysis Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/goal_context.md
   - Perform: Risk identification - identify risks, mitigation strategies, failure points, contingency planning requirements
   - Create: [DOCUMENT_DIRECTORY]/phase_1_analysis/risk_analysis.md (documenting completed risk assessment)

8. Main Agent: Read all foundational analysis documents, synthesize findings
9. **IF CONTRADICTIONS FOUND**: Repeat Phase 1A with clarified scope and conflict resolution instructions
10. **CHECKPOINT 1**: If checkpoints enabled, review foundational analysis and validate direction

**PHASE 1B - STRATEGIC DECOMPOSITION (3 Parallel Sub-Agents):**
11. Deploy THREE parallel sub-agents simultaneously:

    **Decomposition Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/requirements_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/feasibility_analysis.md
    - Perform: Goal decomposition - break goal into phases, milestones, deliverables, component breakdown
    - Create: [DOCUMENT_DIRECTORY]/phase_1_analysis/decomposition_analysis.md (documenting completed decomposition)

    **Resource Analysis Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/context_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/requirements_analysis.md
    - Perform: Resource assessment - analyze resource needs, skill gaps, team composition, infrastructure requirements
    - Create: [DOCUMENT_DIRECTORY]/phase_1_analysis/resource_analysis.md (documenting completed resource assessment)

    **Dependency Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/decomposition_analysis.md (wait for completion)
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/risk_analysis.md
    - Perform: Dependency mapping - identify critical path, integration points, coordination needs, interdependencies
    - Create: [DOCUMENT_DIRECTORY]/phase_1_analysis/dependency_analysis.md (documenting completed dependency mapping)

12. Main Agent: Read all decomposition documents, validate analysis
13. **IF ANALYSIS CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
14. **CHECKPOINT 2**: If checkpoints enabled, review strategic decomposition before solution design

**PHASE 2 - SOLUTION ARCHITECTURE (2 Parallel Sub-Agents):**
15. Deploy TWO sub-agents simultaneously:

    **Solution Architecture Sub-Agent:**
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_1_analysis/
    - Perform: Solution design - design optimal architecture with component relationships, system design, technical approach
    - Create: [DOCUMENT_DIRECTORY]/phase_2_solution_architecture/solution_architecture_analysis.md (documenting completed solution design)

    **Implementation Strategy Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/decomposition_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/resource_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/dependency_analysis.md
    - Perform: Implementation strategy development - create detailed implementation approach, methodology, execution strategy
    - Create: [DOCUMENT_DIRECTORY]/phase_2_solution_architecture/implementation_strategy_analysis.md (documenting completed strategy development)

16. Main Agent: Read solution architecture documents, validate approach
17. **IF SOLUTION CONFLICTS**: Create conflict resolution document and re-run affected sub-agents
18. **CHECKPOINT 3**: If checkpoints enabled, review solution architecture before detailed planning

**PHASE 3 - DETAILED PLANNING (5 Parallel Sub-Agents):**
19. Deploy FIVE parallel sub-agents simultaneously:

    **Timeline Planning Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/decomposition_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/dependency_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_solution_architecture/implementation_strategy_analysis.md
    - Perform: Timeline development - create detailed timeline with critical path analysis, milestone scheduling, dependency management
    - Create: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/timeline_planning_analysis.md (documenting completed timeline planning)

    **Resource Planning Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/resource_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_solution_architecture/solution_architecture_analysis.md
    - Perform: Resource allocation planning - develop resource allocation with team assignments, budget planning, tool procurement
    - Create: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/resource_planning_analysis.md (documenting completed resource planning)

    **Risk Management Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/risk_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_solution_architecture/implementation_strategy_analysis.md
    - Perform: Risk management planning - create risk management plan with mitigation strategies, contingency planning
    - Create: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/risk_management_analysis.md (documenting completed risk planning)

    **Quality Assurance Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/requirements_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_solution_architecture/solution_architecture_analysis.md
    - Perform: Quality assurance planning - design QA framework with testing approaches, acceptance criteria, quality gates
    - Create: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/quality_assurance_analysis.md (documenting completed QA planning)

    **Communication Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/context_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/timeline_planning_analysis.md (wait for completion)
    - Perform: Communication planning - develop stakeholder communication plan, progress tracking, reporting frameworks
    - Create: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/communication_analysis.md (documenting completed communication planning)

20. Main Agent: Read all detailed planning documents, integrate planning components
21. **IF PLANNING CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
22. **CHECKPOINT 4**: If checkpoints enabled, review detailed planning before execution framework

**PHASE 4 - EXECUTION FRAMEWORK (3 Sequential Sub-Agents):**
23. Deploy THREE sub-agents sequentially:

    **Governance Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/communication_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/quality_assurance_analysis.md
    - Perform: Governance framework development - establish governance structure with decision processes, approval workflows, authority matrix
    - Create: [DOCUMENT_DIRECTORY]/phase_4_execution_framework/governance_analysis.md (documenting completed governance framework)

    **Monitoring Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_analysis/requirements_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/timeline_planning_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_4_execution_framework/governance_analysis.md
    - Perform: Monitoring system design - design monitoring systems with KPIs, dashboards, progress tracking mechanisms
    - Create: [DOCUMENT_DIRECTORY]/phase_4_execution_framework/monitoring_analysis.md (documenting completed monitoring design)

    **Adaptation Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_detailed_planning/risk_management_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_4_execution_framework/monitoring_analysis.md
    - Perform: Adaptation framework development - create change management framework with feedback loops, adjustment mechanisms
    - Create: [DOCUMENT_DIRECTORY]/phase_4_execution_framework/adaptation_analysis.md (documenting completed adaptation framework)

24. Main Agent: Read all execution framework documents, compile strategic plan document, update knowledge graph

**DOCUMENT STRUCTURE REQUIREMENTS:**

Each sub-agent document must include:
```markdown
# [Domain] Strategic Analysis
**Agent:** [Sub-Agent Name]
**Phase:** [Phase Number]
**Timestamp:** [ISO Timestamp]
**Documents Read:** [List of input documents]
**Strategic Focus:** [Specific planning domain]

## Executive Summary
[Brief overview of strategic work completed]

## Detailed Strategic Analysis
[Comprehensive analysis within strategic domain]

## Key Deliverables
[Specific strategic outputs and frameworks]

## Implementation Requirements
[Requirements for successful implementation]

## Success Criteria
[Measurable indicators and benchmarks]

## Integration Points
[How work relates to other strategic domains]

## Risk Considerations
[Strategic risks and mitigation approaches]
```

**STRATEGIC PLANNING SCOPE ISOLATION:**
- **Foundation analysis sub-agents focus only on analysis** without attempting strategy or implementation
- **Decomposition sub-agents work within specialization** without overlapping into other analysis areas
- **Solution architecture sub-agents design solutions** without detailed implementation planning
- **Planning sub-agents work within their planning domain** without overlapping responsibilities
- **Execution framework sub-agents create frameworks** without modifying strategic direction
- **Main agent maintains strategic oversight** and handles all integration and decision-making

**CONFLICT RESOLUTION PROTOCOL:**
1. Main Agent identifies contradictions between strategic documents
2. Create strategic_conflict_resolution_[timestamp].md documenting specific conflicts
3. Re-run affected sub-agents with conflict context and additional guidance
4. Continue workflow with updated documents

**COMPLEXITY ADAPTATION:**
- **Simple Goals (< 3 months)**: Use abbreviated workflow with 2-3 phases and reduced sub-agent deployment
- **Medium Goals (3-12 months)**: Use full workflow with standard sub-agent delegation as described
- **Complex Goals (12+ months)**: Use extended workflow with additional specialized sub-agents

**HUMAN FEEDBACK OPTIONS:**
- **Default**: Fully autonomous execution with comprehensive strategic plan
- **Add "WITH CHECKPOINTS"**: Pause after each major phase for review and strategic input
- **Add "REVIEW ANALYSIS"**: Pause only after Phase 1 to confirm foundational analysis
- **Add "REVIEW ARCHITECTURE"**: Pause only after Phase 2 to approve solution approach
- **Add "REVIEW PLANNING"**: Pause only after Phase 3 to review detailed plans

**GOAL TO PLAN:**
[GOAL DESCRIPTION] using document directory [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW ANALYSIS | REVIEW ARCHITECTURE | REVIEW PLANNING]

Begin with Phase 0 goal context preparation and proceed systematically through each strategic planning phase with validation checkpoints.
```

## Usage Instructions

1. **Replace placeholders** with specific information:
   - `[GOAL DESCRIPTION]` - Detailed description including objective, scope, success criteria, constraints, timeline
   - `[DOCUMENT_DIRECTORY]` - Absolute path where documents should be stored (e.g., "/project/strategic-plans/digital-transformation")

2. **Prepare document directory** - Ensure the specified directory exists and is writable

3. **Choose feedback level** by adding optional modifiers for human checkpoints

4. **Complexity determines workflow depth** - Simple goals use abbreviated workflow, complex goals use extended workflow

## Key Benefits of File-Based Communication

- **Comprehensive Strategic Documentation**: Complete preservation of all strategic analysis and planning
- **Decision Traceability**: Clear documentation of strategic decisions and rationale
- **Implementation Readiness**: Detailed planning documentation for successful execution
- **Risk Management**: Systematic risk assessment and mitigation planning throughout process
- **Stakeholder Alignment**: Clear communication planning and governance frameworks
- **Knowledge Building**: Strategic planning patterns and successful approaches captured for future goals

## Document Organization Example

```
/project/strategic-plans/digital-transformation/
├── goal_context.md
├── phase_1_analysis/
│   ├── context_analysis.md
│   ├── requirements_analysis.md
│   ├── feasibility_analysis.md
│   ├── risk_analysis.md
│   ├── decomposition_analysis.md
│   ├── resource_analysis.md
│   └── dependency_analysis.md
├── phase_2_solution_architecture/
│   ├── solution_architecture_analysis.md
│   └── implementation_strategy_analysis.md
├── phase_3_detailed_planning/
│   ├── timeline_planning_analysis.md
│   ├── resource_planning_analysis.md
│   ├── risk_management_analysis.md
│   ├── quality_assurance_analysis.md
│   └── communication_analysis.md
└── phase_4_execution_framework/
    ├── governance_analysis.md
    ├── monitoring_analysis.md
    └── adaptation_analysis.md
```

## Strategic Goal Categories

**Business Objectives:**
- Revenue growth and market expansion
- Operational efficiency improvements
- Customer satisfaction and retention
- Product development and innovation

**Technical Implementation:**
- System modernization and upgrades
- Digital transformation initiatives
- Technology adoption and integration
- Infrastructure improvements

**Organizational Transformation:**
- Culture change and development
- Process improvement and optimization
- Workforce development and training
- Structural reorganization

**Process Improvement:**
- Quality enhancement initiatives
- Cost reduction and optimization
- Automation and digitization
- Compliance and governance

## Advanced Strategic Features

- **Multi-Phase Planning**: Systematic progression from analysis to execution framework
- **Risk Integration**: Comprehensive risk management throughout planning process
- **Stakeholder Alignment**: Clear communication and governance planning
- **Quality Assurance**: Built-in quality gates and acceptance criteria
- **Adaptive Framework**: Change management and adjustment mechanisms
- **Knowledge Transfer**: Strategic patterns and approaches for future planning
