# [WORKFLOW NAME] with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to [WORKFLOW ACTION] for [TARGET DESCRIPTION]. Store [FINDINGS/RESEARCH/ANALYSIS] in [DOCUMENT_DIRECTORY]. Follow this file-based [WORKFLOW TYPE] workflow:

**PHASE 0 - [PREPARATION PHASE NAME]:**
1. Create directories: /[phase1_dir]/, /[phase2_dir]/, /[phase3_dir]/, /[phase4_dir]/
2. [CONTEXT ANALYSIS STEPS]
3. Create: [DOCUMENT_DIRECTORY]/[scope_document].md

**PHASE 1 - [FOUNDATIONAL PHASE NAME] ([NUMBER] Parallel Sub-Agents):**
[IF CONDITIONAL LOGIC NEEDED]:
**PHASE 1A - [FOUNDATIONAL SUB-PHASE] (1 Sub-Agent) - [CONDITION]:**
- Read: [scope_document].md
- Perform: [FOUNDATIONAL ANALYSIS DESCRIPTION]
- Create: /[phase1_dir]/foundational_analysis.md

**PHASE 1B - [TARGETED SUB-PHASE] ([NUMBER] Parallel Sub-Agents):**

Deploy [NUMBER] parallel sub-agents:

**[Sub-Agent 1 Name]:**
- Read: [scope_document].md, foundational_analysis.md OR existing_knowledge_summary.md
- Perform: [SPECIFIC ANALYSIS 1 DESCRIPTION]
- Create: /[phase1_dir]/[output_file_1].md

**[Sub-Agent 2 Name]:**
- Read: [scope_document].md, foundational_analysis.md OR existing_knowledge_summary.md
- Perform: [SPECIFIC ANALYSIS 2 DESCRIPTION]
- Create: /[phase1_dir]/[output_file_2].md

**[Sub-Agent N Name]:**
- Read: [scope_document].md, foundational_analysis.md OR existing_knowledge_summary.md
- Perform: [SPECIFIC ANALYSIS N DESCRIPTION]
- Create: /[phase1_dir]/[output_file_n].md

**PHASE 2 - [PLANNING/SYNTHESIS PHASE NAME] ([NUMBER] Sub-Agent[s]):**
[IF SINGLE SUB-AGENT]:
- Read: All [phase1_dir]/ documents
- Perform: [PLANNING/SYNTHESIS DESCRIPTION]
- Create: /[phase2_dir]/[planning_output].md

[IF MULTIPLE SUB-AGENTS]:
Deploy [NUMBER] parallel sub-agents:

**[Planning Sub-Agent 1 Name]:**
- Read: [specific_input_files].md
- Perform: [PLANNING ACTIVITY 1 DESCRIPTION]
- Create: /[phase2_dir]/[planning_output_1].md

**[Planning Sub-Agent N Name]:**
- Read: [specific_input_files].md
- Perform: [PLANNING ACTIVITY N DESCRIPTION]
- Create: /[phase2_dir]/[planning_output_n].md

**PHASE 3 - [IMPLEMENTATION/EXECUTION PHASE NAME] (Multiple Sub-Agents):**

Deploy [NUMBER] parallel sub-agents:

**[Domain 1] Sub-Agent:**
- Read: [planning_output].md, [relevant_analysis].md
- Perform: [DOMAIN 1 WORK DESCRIPTION]
- Create: /[phase3_dir]/[domain1_output].md

**[Domain 2] Sub-Agent:**
- Read: [planning_output].md, [relevant_analysis].md
- Perform: [DOMAIN 2 WORK DESCRIPTION]
- Create: /[phase3_dir]/[domain2_output].md

**[Domain N] Sub-Agent:**
- Read: [planning_output].md, [relevant_analysis].md
- Perform: [DOMAIN N WORK DESCRIPTION]
- Create: /[phase3_dir]/[domainN_output].md

[IF SEQUENTIAL SUB-AGENTS NEEDED]:
**[Integration] Sub-Agent:** (Sequential)
- Read: All [phase3_dir]/ documents
- Perform: [INTEGRATION DESCRIPTION]
- Create: /[phase3_dir]/[integration_output].md

**[Validation] Sub-Agent:** (Sequential)
- Read: [relevant_analysis].md, [integration_output].md
- Perform: [VALIDATION DESCRIPTION]
- Create: /[phase3_dir]/[validation_output].md

**PHASE 4 - [VERIFICATION/COMPLETION PHASE NAME] ([NUMBER] Sequential Sub-Agents):**

**[Verification 1] Sub-Agent:**
- Read: [relevant_input].md
- Perform: [VERIFICATION 1 DESCRIPTION]
- Create: /[phase4_dir]/[verification1_output].md

**[Verification 2] Sub-Agent:**
- Read: [verification1_output].md, [other_relevant_input].md
- Perform: [VERIFICATION 2 DESCRIPTION]
- Create: /[phase4_dir]/[verification2_output].md

[IF FINAL REPORT NEEDED]:
**[Report] Sub-Agent:**
- Read: All documents from all phases
- Perform: [REPORT COMPILATION DESCRIPTION]
- Create: /[phase4_dir]/[final_report].md

**Document Template:**

"""markdown
# [Domain] [Analysis/Implementation/Review]
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Relevant For:** [Next Phase Agents]

## Executive Summary
[Brief overview]

## Detailed [Findings/Implementation/Analysis]
[Comprehensive work]

## [Integration Points/Data Sources/Cross-Domain Relationships]
[How work relates to other domains]

## [Next Phase Requirements/Key Insights/Recommendations]
[Guidance for next phase or key outcomes]

## [Issues/Conflicts/Confidence Assessment]
[Problems or uncertainties identified]
"""

[IF SCOPE ISOLATION NEEDED]:
**Scope Isolation:**
- [Implementation/Analysis] sub-agents never run [GLOBAL CHECKS] during [DEVELOPMENT/ANALYSIS]
- Each sub-agent works only within assigned domain
- [Global validation/Final integration] occurs in Phase [N]

**Options:** [TARGET DESCRIPTION] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW [PHASE] | REVIEW [PHASE]]
```

## Key Benefits
- **[Benefit 1]**: [Brief description emphasizing file-based advantage]
- **[Benefit 2]**: [Brief description emphasizing documentation preservation]
- **[Benefit 3]**: [Brief description emphasizing knowledge building]
- **[Benefit 4]**: [Brief description emphasizing parallel safety or audit trail]

## Template Usage Instructions

### Required Replacements:

#### Core Workflow Elements:
1. **[WORKFLOW NAME]** - The specific name of your workflow
2. **[WORKFLOW ACTION]** - The main action the workflow performs (e.g., "implement", "analyze", "review")
3. **[TARGET DESCRIPTION]** - What the workflow operates on (e.g., "FEATURE DESCRIPTION", "CODE CHANGES")
4. **[WORKFLOW TYPE]** - Type of workflow (e.g., "implementation", "analysis", "review")
5. **[FINDINGS/RESEARCH/ANALYSIS]** - What type of information is being stored

#### Phase Structure:
6. **[PREPARATION PHASE NAME]** - Name of Phase 0 (e.g., "CONTEXT PREPARATION", "SCOPE ASSESSMENT")
7. **[FOUNDATIONAL PHASE NAME]** - Name of Phase 1 (e.g., "DISCOVERY", "FOUNDATIONAL RESEARCH")
8. **[PLANNING/SYNTHESIS PHASE NAME]** - Name of Phase 2 (e.g., "PLANNING", "COMPETITIVE ANALYSIS")
9. **[IMPLEMENTATION/EXECUTION PHASE NAME]** - Name of Phase 3 (e.g., "IMPLEMENTATION", "DEMAND ANALYSIS")
10. **[VERIFICATION/COMPLETION PHASE NAME]** - Name of Phase 4 (e.g., "VERIFICATION", "STRATEGY")

#### Directory and File Names:
11. **[phase1_dir], [phase2_dir], [phase3_dir], [phase4_dir]** - Directory names for each phase
12. **[scope_document]** - Name of the initial scope document (e.g., "feature_scope", "review_scope")
13. **[output_file_1], [output_file_2], [output_file_n]** - Output file names from Phase 1
14. **[planning_output]** - Output file name from Phase 2
15. **[domain1_output], [domain2_output], [domainN_output]** - Domain-specific output files
16. **[integration_output], [validation_output]** - Sequential sub-agent outputs
17. **[verification1_output], [verification2_output]** - Verification phase outputs
18. **[final_report]** - Final report file name

#### Sub-Agent Definitions:
19. **[Sub-Agent 1 Name], [Sub-Agent 2 Name], [Sub-Agent N Name]** - Names of Phase 1 sub-agents
20. **[Planning Sub-Agent 1 Name], [Planning Sub-Agent N Name]** - Names of Phase 2 sub-agents
21. **[Domain 1], [Domain 2], [Domain N]** - Names of different work domains
22. **[Integration], [Validation]** - Names of sequential sub-agents
23. **[Verification 1], [Verification 2], [Report]** - Names of final phase sub-agents
24. **[NUMBER]** - Number of parallel sub-agents to deploy

#### Work Descriptions:
25. **[CONTEXT ANALYSIS STEPS]** - What happens in Phase 0 preparation
26. **[FOUNDATIONAL ANALYSIS DESCRIPTION]** - What the foundational analysis covers
27. **[SPECIFIC ANALYSIS 1/2/N DESCRIPTION]** - What each targeted analysis covers
28. **[PLANNING/SYNTHESIS DESCRIPTION]** - What the planning phase produces
29. **[PLANNING ACTIVITY 1/N DESCRIPTION]** - What each planning sub-agent does
30. **[DOMAIN 1/2/N WORK DESCRIPTION]** - What each domain sub-agent does
31. **[INTEGRATION DESCRIPTION]** - What the integration sub-agent does
32. **[VALIDATION DESCRIPTION]** - What the validation sub-agent does
33. **[VERIFICATION 1/2 DESCRIPTION]** - What each verification sub-agent does
34. **[REPORT COMPILATION DESCRIPTION]** - What the final report sub-agent does

#### Document References:
35. **[specific_input_files]** - Specific files that sub-agents should read
36. **[relevant_analysis]** - Relevant analysis files for implementation phase
37. **[relevant_input]** - Relevant input files for verification phase
38. **[other_relevant_input]** - Additional input files for final verification

#### Conditional Elements:
39. **[CONDITION]** - Condition for when foundational analysis is needed
40. **[FOUNDATIONAL SUB-PHASE], [TARGETED SUB-PHASE]** - Names of conditional sub-phases

#### Document Template Customization:
41. **[Analysis/Implementation/Review]** - Type of work being documented
42. **[Findings/Implementation/Analysis]** - Type of detailed content
43. **[Integration Points/Data Sources/Cross-Domain Relationships]** - Type of relationship content
44. **[Next Phase Requirements/Key Insights/Recommendations]** - Type of guidance content
45. **[Issues/Conflicts/Confidence Assessment]** - Type of uncertainty content

#### Scope Isolation (if needed):
46. **[Implementation/Analysis]** - Type of sub-agents that need scope isolation
47. **[GLOBAL CHECKS]** - What global operations should be avoided
48. **[DEVELOPMENT/ANALYSIS]** - Phase where global checks are avoided
49. **[Global validation/Final integration]** - What happens in the final phase
50. **[N]** - Phase number where global validation occurs

#### Benefits Customization:
51. **[Benefit 1/2/3/4]** - Specific benefits of your workflow

### Customization Guidelines:

#### Phase Structure Options:
- **Simple workflows**: Use 3-4 phases, remove conditional logic
- **Complex workflows**: Add conditional Phase 1A/1B structure
- **Research workflows**: Include multiple analysis phases
- **Implementation workflows**: Include parallel domain work

#### Sub-Agent Deployment Patterns:
- **Analysis-heavy**: More parallel sub-agents in early phases
- **Implementation-heavy**: More parallel sub-agents in middle phases
- **Validation-heavy**: More sequential sub-agents in final phases

#### Document Flow Design:
- **Linear flow**: Each phase reads from previous phase only
- **Selective flow**: Sub-agents read specific relevant documents
- **Comprehensive flow**: Final phases read from all previous phases

#### Conditional Logic Usage:
- **Knowledge-based**: Different paths based on existing knowledge
- **Complexity-based**: Different paths based on project complexity
- **Context-based**: Different paths based on specific conditions

#### Scope Isolation Application:
- **Implementation workflows**: Prevent global checks during development
- **Analysis workflows**: Prevent cross-domain interference
- **Review workflows**: Maintain domain-specific focus

This template provides the concise, efficient format of minified workflows while maintaining the comprehensive documentation and knowledge preservation benefits of file-based communication.
