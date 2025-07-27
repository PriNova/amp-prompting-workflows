# Minified: Interactive Specification Creation from User Goals

## Workflow Prompt

```
Create comprehensive specification for [USER GOAL DESCRIPTION] using adaptive dialog and systematic analysis:

**PHASE 0 - GOAL CLARITY ASSESSMENT:**
1. Check knowledge graph for related specifications and documentation patterns
2. Analyze goal specificity, clarity, completeness, domain scope
3. Create todo breakdown with todo_write
4. **DECISION POINT**: Assess goal clarity level

**CLARITY BRANCH A - VAGUE/AMBIGUOUS GOALS:**
If goal lacks specificity, domain clarity, or key details:
- **PROGRESSIVE CLARIFICATION**: Ask questions in small batches (1-2 open questions OR use multiple_choice tool)
- **QUESTION PRIORITIZATION**: Start with most fundamental gaps first:
  1. Core problem/purpose (1-2 open questions max)
  2. Users/stakeholders (use multiple_choice if options are clear)
  3. Success criteria (1-2 open questions max)
  4. Technical constraints (use multiple_choice for known options)
  5. Timeline/scope (use multiple_choice for timeframe ranges)
- **ITERATIVE REFINEMENT**: Wait for user response before asking next batch
- **TRANSITION**: Once clarified, proceed to Phase 1

**CLARITY BRANCH B - SPECIFIC GOALS:**
If goal is clear, specific, and actionable:
- **CONFIRMATION**: Briefly confirm understanding with user
- **DIRECT EXECUTION**: Proceed immediately to Phase 1

**PHASE 1 - REQUIREMENTS GATHERING:**
Deploy FOUR parallel sub-agents:
- Functional Requirements: Define core functionality, user interactions, system behaviors, feature scope
- Non-Functional Requirements: Performance, security, scalability, usability, compatibility requirements
- Technical Requirements: Technology stack, architecture constraints, integration needs, platform requirements
- Business Requirements: Success criteria, timeline, budget, compliance, regulatory considerations

**PHASE 2 - STAKEHOLDER & CONTEXT ANALYSIS:**
Deploy THREE parallel sub-agents (with requirements Agent Briefing):
- User Analysis: Identify user personas, use cases, user journeys, accessibility needs
- Technical Context: Analyze existing systems, dependencies, constraints, integration points
- Business Context: Market analysis, competitive landscape, business objectives, ROI considerations

**PHASE 3 - SPECIFICATION ARCHITECTURE:**
- Main agent: Synthesize analysis results, identify specification structure, resolve conflicts
- **VALIDATION CHECKPOINT**: Present high-level approach to user for confirmation
- Deploy TWO sub-agents simultaneously:
  - Document Architecture: Design specification structure with sections, templates, documentation standards
  - Technical Architecture: Define system architecture, component relationships, data flows, interfaces

**PHASE 4 - DETAILED SPECIFICATION:**
Deploy SIX parallel sub-agents:
- Functional Specification: Detailed feature descriptions, user stories, acceptance criteria, workflows
- Technical Specification: System design, API definitions, data models, architecture diagrams
- Interface Specification: UI/UX requirements, wireframes, interaction patterns, design guidelines
- Integration Specification: External system interfaces, data exchange, communication protocols
- Testing Specification: Test strategies, test cases, quality assurance criteria, validation methods
- Implementation Specification: Development guidelines, coding standards, deployment procedures

**PHASE 5 - VALIDATION & REFINEMENT:**
- **DRAFT REVIEW**: Present specification draft to user for feedback
- Deploy FOUR sequential sub-agents based on feedback:
  - Completeness Review: Verify all requirements covered, identify gaps, ensure consistency
  - Feasibility Validation: Assess technical feasibility, resource requirements, timeline realism
  - Stakeholder Alignment: Validate against business objectives, user needs, technical constraints
  - Documentation Quality: Review clarity, completeness, usability, maintainability

**INTERACTIVE ELEMENTS:**
- **Progressive Questioning**: Ask 1-2 open questions at a time, wait for response
- **Multiple Choice Tool**: Use for binary (yes/no) or clear option-based questions
- **Confirmation Points**: Verify understanding before major work phases
- **Validation Checkpoints**: Present drafts and approaches for user feedback
- **Iterative Refinement**: Adjust based on user input throughout process

**QUESTION GUIDELINES:**
- **Open Questions (1-2 max per interaction)**: "What specific problem are you trying to solve?" "What would success look like?"
- **Multiple Choice Questions**: Use multiple_choice tool for:
  - Binary choices: "Is this a web application or mobile app?"
  - Timeline ranges: "What's your target timeline?" (options: <1 month, 1-3 months, 3+ months)
  - User types: "Who are the primary users?" (options: Internal team, External customers, Both)
  - Technical preferences: "Do you have technology preferences?" (options: Use existing stack, Open to suggestions, Specific requirements)
- **Follow-up Clarification**: "When you say [user term], could you elaborate on [specific aspect]?"

**COMPLEXITY ADAPTATION:**
- Vague Goals: Extended clarification dialog before specification work
- Medium Goals: Standard workflow with confirmation checkpoints
- Complex Goals: Additional validation rounds and stakeholder consideration

**SCOPE ISOLATION:**
- Requirements sub-agents focus only on assigned domain without attempting design
- Specification sub-agents work within specialization without overlapping into other areas
- Validation sub-agents review only assigned aspects without attempting corrections

**FEEDBACK OPTIONS:**
Default: Interactive Dialog | AUTONOMOUS: Skip clarification | WITH CHECKPOINTS: All phases | REVIEW SPECIFICATION: Phase 4 only

**USER GOAL TO SPECIFY:**
[USER GOAL DESCRIPTION] [OPTIONAL MODIFIER]
```

## Key Benefits
- **Adaptive Dialog**: Automatically adjusts from clarification questions to full specification based on goal clarity
- **Interactive Refinement**: Continuous user feedback ensures specifications match actual needs
- **Comprehensive Coverage**: Six specialized domains ensure no critical requirements overlooked

## Usage
Replace `[USER GOAL DESCRIPTION]` with your goal or project. The workflow will automatically assess clarity and either ask clarifying questions or proceed with specification creation. Add optional modifiers for feedback control.
