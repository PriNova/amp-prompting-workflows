# How to [WORKFLOW NAME] Using File-Based Sub-Agent Communication

## Overview
This workflow [BRIEF WORKFLOW DESCRIPTION] by using strategic sub-agent delegation with persistent file-based communication. Each sub-agent documents their findings, enabling precise knowledge transfer and reusable insights.

## Complete Workflow Prompt

```
I need to [WORKFLOW ACTION] for [TARGET DESCRIPTION]. Store all sub-agent findings in [DOCUMENT_DIRECTORY]. Follow this file-based communication workflow:

**PHASE 0 - [PREPARATION PHASE NAME] (Main Agent):**
1. Create document directory structure in [DOCUMENT_DIRECTORY]:
   - /phase_1_[phase1_name]/
   - /phase_2_[phase2_name]/
   - /phase_3_[phase3_name]/
   - /phase_4_[phase4_name]/
2. Check existing knowledge graph for [DOMAIN] understanding
3. **IF SUBSTANTIAL KNOWLEDGE EXISTS:**
   - Review stored [DOMAIN KNOWLEDGE TYPES]
   - Create targeted [ANALYSIS TYPE] plan focusing only on unknown areas
   - Create: [DOCUMENT_DIRECTORY]/existing_knowledge_summary.md
   - Proceed with abbreviated [DISCOVERY/ANALYSIS] ([PHASE REFERENCE])
4. **IF MINIMAL KNOWLEDGE EXISTS:**
   - Proceed with full [DISCOVERY/ANALYSIS] workflow ([PHASE REFERENCE])
5. Create initial todo breakdown using todo_write
6. Create: [DOCUMENT_DIRECTORY]/[SCOPE_DOCUMENT_NAME].md (documenting [SCOPE CONTENT])

**PHASE 1A - [FOUNDATIONAL PHASE NAME] (Single Sub-Agent) - For [NEW CONTEXT CONDITION]:**
7. Deploy ONE sub-agent for [FOUNDATIONAL ANALYSIS]:
   - Read: [DOCUMENT_DIRECTORY]/[SCOPE_DOCUMENT_NAME].md
   - Perform: [COMPREHENSIVE FOUNDATIONAL ANALYSIS DESCRIPTION]
   - Create: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/foundational_analysis.md (documenting completed foundational analysis)

**PHASE 1B - [TARGETED ANALYSIS PHASE NAME] ([NUMBER] Parallel Sub-Agents):**
8. Deploy [NUMBER] parallel sub-agents simultaneously:

   **[Sub-Agent 1 Name]:**
   - Read: [DOCUMENT_DIRECTORY]/[SCOPE_DOCUMENT_NAME].md
   - Read: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/foundational_analysis.md (if exists) OR [DOCUMENT_DIRECTORY]/existing_knowledge_summary.md
   - Perform: [SPECIFIC ANALYSIS DESCRIPTION]
   - Create: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/[output_file_1].md (documenting completed [analysis type])

   **[Sub-Agent 2 Name]:**
   - Read: [DOCUMENT_DIRECTORY]/[SCOPE_DOCUMENT_NAME].md
   - Read: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/foundational_analysis.md (if exists) OR [DOCUMENT_DIRECTORY]/existing_knowledge_summary.md
   - Perform: [SPECIFIC ANALYSIS DESCRIPTION]
   - Create: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/[output_file_2].md (documenting completed [analysis type])

   **[Sub-Agent N Name]:**
   - Read: [DOCUMENT_DIRECTORY]/[SCOPE_DOCUMENT_NAME].md
   - Read: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/foundational_analysis.md (if exists) OR [DOCUMENT_DIRECTORY]/existing_knowledge_summary.md
   - Perform: [SPECIFIC ANALYSIS DESCRIPTION]
   - Create: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/[output_file_n].md (documenting completed [analysis type])

9. Main Agent: Read all [ANALYSIS TYPE] documents, check for contradictions, merge with existing knowledge
10. **IF CONTRADICTIONS FOUND**: Repeat Phase 1B with clarified scope and conflict resolution instructions
11. **CHECKPOINT 1**: If checkpoints enabled, summarize [ANALYSIS TYPE] findings and confirm approach

**PHASE 2 - [SYNTHESIS/PLANNING PHASE NAME] (Main Agent + 1 Sub-Agent):**
12. Main Agent: Synthesize discoveries, update todos with specific [IMPLEMENTATION/EXECUTION] tasks
13. Deploy ONE sub-agent for [PLANNING/ARCHITECTURE] planning:
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/
    - Perform: [PLANNING/ARCHITECTURE DESCRIPTION]
    - Create: [DOCUMENT_DIRECTORY]/phase_2_[phase2_name]/[planning_output].md (documenting completed planning analysis)
14. Main Agent: Review [planning output], create dependency-ordered [implementation/execution] strategy
15. **CHECKPOINT 2**: If checkpoints enabled, present [planning output] and [strategy] for approval

**PHASE 3 - [IMPLEMENTATION/EXECUTION PHASE NAME] (Multiple Sub-Agents):**
16. Deploy independent sub-agents in parallel:

    **[Domain 1] Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_[phase2_name]/[planning_output].md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/[relevant_analysis].md
    - Perform: [Domain 1 implementation/execution description]
    - Create: [DOCUMENT_DIRECTORY]/phase_3_[phase3_name]/[domain1_output].md (documenting completed [domain 1] work)

    **[Domain 2] Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_[phase2_name]/[planning_output].md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/[relevant_analysis].md
    - Perform: [Domain 2 implementation/execution description]
    - Create: [DOCUMENT_DIRECTORY]/phase_3_[phase3_name]/[domain2_output].md (documenting completed [domain 2] work)

    **[Domain N] Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_[phase2_name]/[planning_output].md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/[relevant_analysis].md
    - Perform: [Domain N implementation/execution description]
    - Create: [DOCUMENT_DIRECTORY]/phase_3_[phase3_name]/[domainN_output].md (documenting completed [domain N] work)

17. Deploy dependent sub-agents sequentially:

    **[Integration] Sub-Agent:**
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_3_[phase3_name]/
    - Perform: [Integration description]
    - Create: [DOCUMENT_DIRECTORY]/phase_3_[phase3_name]/[integration_output].md (documenting completed integration work)

    **[Validation] Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/[validation_relevant_analysis].md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_[phase3_name]/[integration_output].md
    - Perform: [Validation description]
    - Create: [DOCUMENT_DIRECTORY]/phase_3_[phase3_name]/[validation_output].md (documenting completed validation work)

18. Main Agent: Track progress, update existing knowledge graph with new observations, update todos as completed
19. **CHECKPOINT 3**: If checkpoints enabled, summarize [implementation/execution] and confirm [validation] approach

**PHASE 4 - [VERIFICATION/COMPLETION PHASE NAME] (Sequential Sub-Agents):**
20. Deploy [NUMBER] sub-agents sequentially:

    **[Verification 1] Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_[phase1_name]/[relevant_analysis].md
    - Perform: [Verification 1 description]
    - Create: [DOCUMENT_DIRECTORY]/phase_4_[phase4_name]/[verification1_output].md (documenting verification results)

    **[Verification 2] Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_[phase3_name]/[integration_output].md
    - Read: [DOCUMENT_DIRECTORY]/phase_4_[phase4_name]/[verification1_output].md
    - Perform: [Verification 2 description]
    - Create: [DOCUMENT_DIRECTORY]/phase_4_[phase4_name]/[verification2_output].md (documenting validation results)

21. Main Agent: Handle any failures with rollback strategy, final knowledge graph updates and enhancements

**DOCUMENT STRUCTURE REQUIREMENTS:**

Each sub-agent document must include:

"""markdown
# [Domain] Analysis/Implementation
**Agent:** [Sub-Agent Name]
**Phase:** [Phase Number]
**Timestamp:** [ISO Timestamp]
**Documents Read:** [List of input documents]
**Relevant For Next Phase:** [List of domains/agents that should read this]

## Executive Summary
[Brief overview of work completed]

## Detailed Findings/Implementation
[Comprehensive analysis or implementation details]

## Integration Points
[How findings/work relate to other domains]

## Next Phase Requirements
[What subsequent phases need to know]

## Issues/Conflicts
[Any problems or contradictions identified]
"""

**[SCOPE ISOLATION TITLE]:**
- **[Implementation/Analysis] sub-agents never run [GLOBAL CHECKS]** during [development/analysis] phase
- **Each sub-agent only works within their assigned domain** and ignores errors outside their scope
- **Domain boundaries**: [Domain 1] ([domain 1 scope]), [Domain 2] ([domain 2 scope]), [Domain N] ([domain N scope])
- **[File-specific/Domain-specific] validation only** during [implementation/analysis] - global validation occurs in Phase 4
- **[Integration] sub-agent** [integration timing and scope]

**CONFLICT RESOLUTION PROTOCOL:**
1. Main Agent identifies contradictions between documents
2. Create conflict_resolution_[timestamp].md documenting specific conflicts
3. Re-run affected sub-agents with conflict context and additional guidance
4. Continue workflow with updated documents

**HUMAN FEEDBACK OPTIONS:**
- **Default**: Fully autonomous execution with final summary
- **Add "WITH CHECKPOINTS"**: Pause after each major phase for review and approval
- **Add "REVIEW [PHASE NAME]"**: Pause only after [Phase Description] for [specific approval type] before [next phase]
- **Add "REVIEW [PHASE NAME]"**: Pause only after [Phase Description] to review [specific content] before [next phase]

**[TARGET DESCRIPTION] TO [ACTION]:**
[TARGET PLACEHOLDER] using document directory [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW [PHASE] | REVIEW [PHASE]]

Begin with Phase 0 and proceed systematically through each phase with proper validation checkpoints.
```

## Usage Instructions

1. **Replace placeholders** with specific information:
   - `[TARGET PLACEHOLDER]` - [Description of what user should input]
   - `[DOCUMENT_DIRECTORY]` - Absolute path where documents should be stored (e.g., "[example path]")

2. **Prepare document directory** - Ensure the specified directory exists and is writable

3. **Choose feedback level** by adding optional modifiers for human checkpoints

4. **For subsequent [workflow type]** in the same [context], this workflow will automatically leverage existing knowledge

## Key Benefits of File-Based Communication

- **Complete Knowledge Preservation**: No information loss through summarization
- **Cumulative Learning**: Each [workflow instance] builds upon detailed [domain] documentation
- **Parallel Safety**: Sub-agents work independently without context interference
- **Selective Context Loading**: Agents only read documents relevant to their domain
- **Persistent Insights**: Documents remain available for future [workflow type] development
- **Conflict Detection**: Systematic comparison reveals contradictions and gaps
- **Audit Trail**: Complete record of [discovery/analysis], planning, and [implementation/execution] decisions

## Document Organization Example

```
[example_path]/
├── [scope_document_name].md
├── existing_knowledge_summary.md (if applicable)
├── phase_1_[phase1_name]/
│   ├── foundational_analysis.md
│   ├── [output_file_1].md
│   ├── [output_file_2].md
│   └── [output_file_n].md
├── phase_2_[phase2_name]/
│   └── [planning_output].md
├── phase_3_[phase3_name]/
│   ├── [domain1_output].md
│   ├── [domain2_output].md
│   ├── [domainN_output].md
│   ├── [integration_output].md
│   └── [validation_output].md
└── phase_4_[phase4_name]/
    ├── [verification1_output].md
    └── [verification2_output].md
```

## Knowledge Enhancement Benefits

- **[Domain] Understanding**: Persistent documentation of [domain-specific patterns and knowledge]
- **[Implementation/Execution] Patterns**: Reusable approaches for similar [workflow instances]
- **[Validation] Strategies**: Documented [validation] patterns for consistent quality
- **Integration Points**: Clear understanding of how components connect
- **[Development/Process] Workflow**: Captured [workflow-specific processes]

## Common Pitfalls Avoided

- **Information Loss**: Complete findings preserved in structured documents
- **Context Interference**: Sub-agents work with clean, targeted document context
- **[Discovery/Analysis] Redundancy**: Documented findings prevent re-analyzing known areas
- **[Implementation/Execution] Conflicts**: Clear domain boundaries prevent parallel work interference
- **Knowledge Fragmentation**: Centralized document repository maintains continuity
- **[Validation] Gaps**: Documented [validation] patterns ensure comprehensive coverage

## Template Usage Instructions

### Required Replacements:

#### Core Workflow Elements:
1. **[WORKFLOW NAME]** - The specific name of your workflow
2. **[WORKFLOW ACTION]** - The main action the workflow performs
3. **[TARGET DESCRIPTION]** - What the workflow operates on
4. **[TARGET PLACEHOLDER]** - The placeholder users replace with their specific input
5. **[ACTION]** - The action verb for the final prompt
6. **[DOMAIN]** - The primary domain of work

#### Phase Customization:
7. **[phase1_name], [phase2_name], etc.** - Short names for each phase directory
8. **[PREPARATION PHASE NAME]** - Name of the initial setup phase
9. **[FOUNDATIONAL PHASE NAME]** - Name of the foundational analysis phase
10. **[TARGETED ANALYSIS PHASE NAME]** - Name of the targeted analysis phase
11. **[SYNTHESIS/PLANNING PHASE NAME]** - Name of the planning phase
12. **[IMPLEMENTATION/EXECUTION PHASE NAME]** - Name of the main work phase
13. **[VERIFICATION/COMPLETION PHASE NAME]** - Name of the final verification phase

#### Document and File Names:
14. **[SCOPE_DOCUMENT_NAME]** - Name of the initial scope document
15. **[SCOPE CONTENT]** - Description of what goes in the scope document
16. **[output_file_1], [output_file_2], etc.** - Names of output files from each sub-agent
17. **[planning_output]** - Name of the planning phase output file
18. **[domain1_output], [domain2_output], etc.** - Names of domain-specific output files
19. **[integration_output]** - Name of the integration output file
20. **[validation_output]** - Name of the validation output file
21. **[verification1_output], [verification2_output]** - Names of verification output files

#### Sub-Agent and Domain Definitions:
22. **[Sub-Agent 1 Name], [Sub-Agent 2 Name], etc.** - Names of specific sub-agents
23. **[Domain 1], [Domain 2], etc.** - Names of different work domains
24. **[NUMBER]** - Number of parallel sub-agents to deploy

#### Scope and Process Descriptions:
25. **[COMPREHENSIVE FOUNDATIONAL ANALYSIS DESCRIPTION]** - What the foundational analysis covers
26. **[SPECIFIC ANALYSIS DESCRIPTION]** - What each targeted analysis covers
27. **[PLANNING/ARCHITECTURE DESCRIPTION]** - What the planning phase produces
28. **[Domain X implementation/execution description]** - What each domain sub-agent does
29. **[Integration description]** - What the integration sub-agent does
30. **[Validation description]** - What the validation sub-agent does
31. **[Verification 1/2 description]** - What each verification sub-agent does

#### Conditional Logic and Context:
32. **[NEW CONTEXT CONDITION]** - Condition for when foundational analysis is needed
33. **[DOMAIN KNOWLEDGE TYPES]** - Types of knowledge stored in the knowledge graph
34. **[ANALYSIS TYPE]** - Type of analysis being performed

#### Scope Isolation and Technical Details:
35. **[SCOPE ISOLATION TITLE]** - Title for the scope isolation section
36. **[GLOBAL CHECKS]** - What global operations should be avoided
37. **[development/analysis]** - The phase where global checks are avoided
38. **[domain 1 scope], [domain 2 scope], etc.** - Specific scope boundaries for each domain

#### Examples and Paths:
39. **[example path]** - Example document directory path
40. **[example_path]** - Example path for document organization
41. **[Description of what user should input]** - Help text for the target placeholder
42. **[workflow type]** - Type of workflow for usage instructions
43. **[context]** - Context where the workflow is reused
44. **[workflow instance]** - Instance of the workflow being executed
45. **[domain-specific patterns and knowledge]** - Domain-specific knowledge types
46. **[workflow-specific processes]** - Processes specific to this workflow

### Customization Guidelines:

#### Phase Structure:
- Adjust the number of phases based on your workflow complexity
- Modify phase names to reflect your specific process
- Add or remove conditional logic (Phase 1A vs 1B) as needed

#### Sub-Agent Deployment:
- Customize the number and types of sub-agents for each phase
- Define clear domain boundaries and responsibilities
- Specify which documents each sub-agent should read

#### Document Structure:
- Adapt the document organization to your workflow needs
- Define meaningful file names that reflect the content
- Ensure clear dependencies between documents

#### Scope Isolation:
- Define specific boundaries for your workflow domains
- Identify what global operations should be avoided during parallel work
- Specify when and how integration occurs

#### Feedback and Checkpoints:
- Identify the most valuable phases for human review
- Customize checkpoint descriptions for your specific workflow
- Define clear review criteria for each checkpoint
