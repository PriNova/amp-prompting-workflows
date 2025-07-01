# Idea Manifestation with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to manifest [IDEA DESCRIPTION] from concept to reality. Store findings in [DOCUMENT_DIRECTORY]. Follow this file-based manifestation workflow:

**PHASE 0 - IDEA SCOPE:**
1. Create directories: /ideation/, /evaluation/, /planning/, /execution/, /testing/, /launch/
2. Analyze idea category, scope level, complexity, resource requirements
3. Create: [DOCUMENT_DIRECTORY]/idea_context.md

**PHASE 1 - BRAINSTORMING & REFINEMENT (3 Parallel Sub-Agents):**

**Creative Expansion Sub-Agent:**
- Read: idea_context.md
- Perform: Wide range of related ideas, variations, creative alternatives
- Create: /ideation/creative_expansion_analysis.md

**Idea Synthesis Sub-Agent:**
- Read: idea_context.md
- Perform: Concept refinement, combinations, concrete idea development
- Create: /ideation/idea_synthesis_analysis.md

**Documentation Sub-Agent:**
- Read: idea_context.md
- Perform: Output capture, thematic organization, structured repository
- Create: /ideation/idea_documentation_analysis.md

**PHASE 2 - EVALUATION & SELECTION (4 Parallel Sub-Agents):**

**Criteria Definition Sub-Agent:**
- Read: idea_context.md, idea_synthesis_analysis.md
- Perform: Evaluation criteria establishment, scoring framework creation
- Create: /evaluation/criteria_definition_analysis.md

**Feasibility Analysis Sub-Agent:**
- Read: idea_synthesis_analysis.md, criteria_definition_analysis.md
- Perform: Technical feasibility, resource requirements, complexity evaluation
- Create: /evaluation/feasibility_analysis.md

**Market Assessment Sub-Agent:**
- Read: idea_synthesis_analysis.md, criteria_definition_analysis.md
- Perform: Demand evaluation, competition analysis, commercial viability
- Create: /evaluation/market_assessment_analysis.md

**Selection Sub-Agent:**
- Read: feasibility_analysis.md, market_assessment_analysis.md
- Perform: Idea scoring, viability ranking, final candidate recommendation
- Create: /evaluation/selection_analysis.md

**PHASE 3 - PLANNING & STRATEGY (5 Parallel Sub-Agents):**

**Project Planning Sub-Agent:**
- Read: selection_analysis.md, feasibility_analysis.md
- Perform: Step-by-step plan, tasks, milestones, project structure
- Create: /planning/project_planning_analysis.md

**Resource Planning Sub-Agent:**
- Read: feasibility_analysis.md, idea_context.md
- Perform: Resource identification, acquisition strategy, budget planning
- Create: /planning/resource_planning_analysis.md

**Timeline Management Sub-Agent:**
- Read: project_planning_analysis.md, resource_planning_analysis.md
- Perform: Realistic timeline, dependencies, milestone scheduling
- Create: /planning/timeline_management_analysis.md

**Risk Assessment Sub-Agent:**
- Read: feasibility_analysis.md, market_assessment_analysis.md
- Perform: Challenge identification, mitigation strategies, contingency planning
- Create: /planning/risk_assessment_analysis.md

**Success Metrics Sub-Agent:**
- Read: idea_context.md, selection_analysis.md
- Perform: Measurable criteria, KPIs, evaluation frameworks
- Create: /planning/success_metrics_analysis.md

**PHASE 4 - EXECUTION (3 Sequential Sub-Agents):**

**Execution Coordination Sub-Agent:**
- Read: project_planning_analysis.md, timeline_management_analysis.md
- Perform: Execution initiation, workflow coordination, implementation start
- Create: /execution/execution_coordination_analysis.md

**Progress Tracking Sub-Agent:**
- Read: execution_coordination_analysis.md, success_metrics_analysis.md
- Perform: Progress monitoring, milestone tracking, KPI measurement
- Create: /execution/progress_tracking_analysis.md

**Adaptation Management Sub-Agent:**
- Read: progress_tracking_analysis.md, risk_assessment_analysis.md
- Perform: Adjustment handling, challenge management, adaptation execution
- Create: /execution/adaptation_management_analysis.md

**PHASE 5 - TESTING & REFINEMENT (4 Parallel Sub-Agents):**

**Prototype Development Sub-Agent:**
- Read: execution_coordination_analysis.md, project_planning_analysis.md
- Perform: MVP/prototype creation, testable version development
- Create: /testing/prototype_development_analysis.md

**Feedback Collection Sub-Agent:**
- Read: prototype_development_analysis.md, market_assessment_analysis.md
- Perform: Feedback strategy, target user input, testing data collection
- Create: /testing/feedback_collection_analysis.md

**Analysis & Iteration Sub-Agent:**
- Read: feedback_collection_analysis.md, success_metrics_analysis.md
- Perform: Feedback analysis, improvement recommendations, iteration planning
- Create: /testing/analysis_iteration_analysis.md

**Quality Assurance Sub-Agent:**
- Read: prototype_development_analysis.md, idea_context.md
- Perform: Functionality testing, requirement validation, quality standards
- Create: /testing/quality_assurance_analysis.md

**PHASE 6 - LAUNCH (3 Sequential Sub-Agents):**

**Launch Preparation Sub-Agent:**
- Read: quality_assurance_analysis.md, analysis_iteration_analysis.md
- Perform: Final preparation, launch materials, pre-launch checklist
- Create: /launch/launch_preparation_analysis.md

**Launch Execution Sub-Agent:**
- Read: launch_preparation_analysis.md, success_metrics_analysis.md
- Perform: Launch execution, performance monitoring, initial metrics
- Create: /launch/launch_execution_analysis.md

**Post-Launch Evaluation Sub-Agent:**
- Read: launch_execution_analysis.md, success_metrics_analysis.md
- Perform: Success evaluation, feedback gathering, objective assessment
- Create: /launch/post_launch_evaluation_analysis.md

**Document Template:**

"""markdown
# [Domain] Analysis/Implementation
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Development Focus:** [Domain]

## Executive Summary
[Brief overview]

## Detailed Analysis/Implementation
[Comprehensive work]

## Key Deliverables
[Specific outputs]

## Success Criteria
[Completion indicators]

## Integration Points
[Cross-domain relationships]

## Next Phase Requirements
[Guidance for next phase]

## Risks and Mitigation
[Risk management]
"""

**Complexity Adaptation:**
- Simple Ideas (< 1 month): Abbreviated workflow with 3-4 phases
- Medium Ideas (1-6 months): Full workflow as described
- Complex Ideas (6+ months): Extended workflow with additional sub-agents

**Options:** [IDEA DESCRIPTION] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW EVALUATION | REVIEW PLANNING | REVIEW TESTING]
```

## Key Benefits
- **Complete Development Documentation**: Full idea evolution from concept to reality
- **Decision Traceability**: Clear documentation of evaluation and selection rationale
- **Implementation Guidance**: Detailed planning and execution for successful delivery
- **Quality Assurance**: Systematic testing and refinement documentation
