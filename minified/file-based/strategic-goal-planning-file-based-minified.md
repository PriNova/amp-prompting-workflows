# Strategic Goal Planning with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to create strategic plan for [GOAL DESCRIPTION]. Store findings in [DOCUMENT_DIRECTORY]. Follow this file-based strategic planning workflow:

**PHASE 0 - GOAL CONTEXT:**
1. Create directories: /analysis/, /architecture/, /planning/, /framework/
2. Analyze goal category, scope level, complexity, resource implications
3. Create: [DOCUMENT_DIRECTORY]/goal_context.md

**PHASE 1A - FOUNDATIONAL ANALYSIS (4 Parallel Sub-Agents):**

**Context Analysis Sub-Agent:**
- Read: goal_context.md
- Perform: Current state, systems, stakeholders, environment, baseline conditions
- Create: /analysis/context_analysis.md

**Requirements Analysis Sub-Agent:**
- Read: goal_context.md
- Perform: Detailed requirements, constraints, dependencies, success metrics
- Create: /analysis/requirements_analysis.md

**Feasibility Analysis Sub-Agent:**
- Read: goal_context.md
- Perform: Technical feasibility, resource availability, timeline viability
- Create: /analysis/feasibility_analysis.md

**Risk Analysis Sub-Agent:**
- Read: goal_context.md
- Perform: Risk identification, mitigation strategies, failure points
- Create: /analysis/risk_analysis.md

**PHASE 1B - STRATEGIC DECOMPOSITION (3 Parallel Sub-Agents):**

**Decomposition Sub-Agent:**
- Read: requirements_analysis.md, feasibility_analysis.md
- Perform: Goal breakdown into phases, milestones, deliverables
- Create: /analysis/decomposition_analysis.md

**Resource Analysis Sub-Agent:**
- Read: context_analysis.md, requirements_analysis.md
- Perform: Resource needs, skill gaps, team composition, infrastructure
- Create: /analysis/resource_analysis.md

**Dependency Sub-Agent:**
- Read: decomposition_analysis.md, risk_analysis.md
- Perform: Critical path, integration points, coordination needs
- Create: /analysis/dependency_analysis.md

**PHASE 2 - SOLUTION ARCHITECTURE (2 Parallel Sub-Agents):**

**Solution Architecture Sub-Agent:**
- Read: All analysis/ documents
- Perform: Optimal architecture design, component relationships, technical approach
- Create: /architecture/solution_architecture_analysis.md

**Implementation Strategy Sub-Agent:**
- Read: decomposition_analysis.md, resource_analysis.md, dependency_analysis.md
- Perform: Implementation approach, methodology, execution strategy
- Create: /architecture/implementation_strategy_analysis.md

**PHASE 3 - DETAILED PLANNING (5 Parallel Sub-Agents):**

**Timeline Planning Sub-Agent:**
- Read: decomposition_analysis.md, dependency_analysis.md, implementation_strategy_analysis.md
- Perform: Detailed timeline, critical path analysis, milestone scheduling
- Create: /planning/timeline_planning_analysis.md

**Resource Planning Sub-Agent:**
- Read: resource_analysis.md, solution_architecture_analysis.md
- Perform: Resource allocation, team assignments, budget planning
- Create: /planning/resource_planning_analysis.md

**Risk Management Sub-Agent:**
- Read: risk_analysis.md, implementation_strategy_analysis.md
- Perform: Risk management plan, mitigation strategies, contingency planning
- Create: /planning/risk_management_analysis.md

**Quality Assurance Sub-Agent:**
- Read: requirements_analysis.md, solution_architecture_analysis.md
- Perform: QA framework, testing approaches, acceptance criteria
- Create: /planning/quality_assurance_analysis.md

**Communication Sub-Agent:**
- Read: context_analysis.md, timeline_planning_analysis.md
- Perform: Stakeholder communication, progress tracking, reporting frameworks
- Create: /planning/communication_analysis.md

**PHASE 4 - EXECUTION FRAMEWORK (3 Sequential Sub-Agents):**

**Governance Sub-Agent:**
- Read: communication_analysis.md, quality_assurance_analysis.md
- Perform: Governance structure, decision processes, approval workflows
- Create: /framework/governance_analysis.md

**Monitoring Sub-Agent:**
- Read: requirements_analysis.md, timeline_planning_analysis.md, governance_analysis.md
- Perform: Monitoring systems, KPIs, dashboards, progress tracking
- Create: /framework/monitoring_analysis.md

**Adaptation Sub-Agent:**
- Read: risk_management_analysis.md, monitoring_analysis.md
- Perform: Change management framework, feedback loops, adjustment mechanisms
- Create: /framework/adaptation_analysis.md

**Document Template:**
```markdown
# [Domain] Strategic Analysis
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Strategic Focus:** [Domain]

## Executive Summary
[Brief overview]

## Detailed Strategic Analysis
[Comprehensive analysis]

## Key Deliverables
[Strategic outputs and frameworks]

## Implementation Requirements
[Requirements for success]

## Success Criteria
[Measurable indicators]

## Integration Points
[Cross-domain relationships]

## Risk Considerations
[Strategic risks and mitigation]
```

**Complexity Adaptation:**
- Simple Goals (< 3 months): Abbreviated workflow with 2-3 phases
- Medium Goals (3-12 months): Full workflow as described
- Complex Goals (12+ months): Extended workflow with additional sub-agents

**Options:** [GOAL DESCRIPTION] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW ANALYSIS | REVIEW ARCHITECTURE | REVIEW PLANNING]
```

## Key Benefits
- **Comprehensive Strategic Documentation**: Complete preservation of all analysis and planning
- **Decision Traceability**: Clear documentation of strategic decisions and rationale
- **Implementation Readiness**: Detailed planning for successful execution
- **Risk Management**: Systematic assessment and mitigation planning
