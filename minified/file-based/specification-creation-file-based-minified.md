# Interactive Specification Creation with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to create comprehensive specification for [USER GOAL DESCRIPTION]. Store findings in [DOCUMENT_DIRECTORY]. Follow this file-based interactive specification workflow:

**PHASE 0 - GOAL CLARITY ASSESSMENT:**
1. Create directories: /requirements/, /context/, /architecture/, /specification/, /validation/
2. Analyze goal specificity, clarity, completeness, domain scope
3. Create: [DOCUMENT_DIRECTORY]/goal_assessment.md
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
- **DOCUMENTATION**: Update goal_assessment.md with clarified information
- **TRANSITION**: Once clarified, proceed to Phase 1

**CLARITY BRANCH B - SPECIFIC GOALS:**
If goal is clear, specific, and actionable:
- **CONFIRMATION**: Briefly confirm understanding with user
- **DIRECT EXECUTION**: Proceed immediately to Phase 1

**PHASE 1 - REQUIREMENTS GATHERING (4 Parallel Sub-Agents):**

**Functional Requirements Sub-Agent:**
- Read: goal_assessment.md
- Perform: Core functionality, user interactions, system behaviors, feature scope
- Create: /requirements/functional_requirements_analysis.md

**Non-Functional Requirements Sub-Agent:**
- Read: goal_assessment.md
- Perform: Performance, security, scalability, usability, compatibility requirements
- Create: /requirements/non_functional_requirements_analysis.md

**Technical Requirements Sub-Agent:**
- Read: goal_assessment.md
- Perform: Technology stack, architecture constraints, integration needs, platform requirements
- Create: /requirements/technical_requirements_analysis.md

**Business Requirements Sub-Agent:**
- Read: goal_assessment.md
- Perform: Success criteria, timeline, budget, compliance, regulatory considerations
- Create: /requirements/business_requirements_analysis.md

**PHASE 2 - STAKEHOLDER & CONTEXT ANALYSIS (3 Parallel Sub-Agents):**

**User Analysis Sub-Agent:**
- Read: functional_requirements_analysis.md, business_requirements_analysis.md
- Perform: User personas, use cases, user journeys, accessibility needs
- Create: /context/user_analysis.md

**Technical Context Sub-Agent:**
- Read: technical_requirements_analysis.md, non_functional_requirements_analysis.md
- Perform: Existing systems, dependencies, constraints, integration points
- Create: /context/technical_context_analysis.md

**Business Context Sub-Agent:**
- Read: business_requirements_analysis.md, user_analysis.md
- Perform: Market analysis, competitive landscape, business objectives, ROI considerations
- Create: /context/business_context_analysis.md

**PHASE 3 - SPECIFICATION ARCHITECTURE (2 Parallel Sub-Agents):**

**VALIDATION CHECKPOINT**: Present high-level approach to user for confirmation

**Document Architecture Sub-Agent:**
- Read: All requirements/ and context/ documents
- Perform: Specification structure design, sections, templates, documentation standards
- Create: /architecture/document_architecture_analysis.md

**Technical Architecture Sub-Agent:**
- Read: technical_requirements_analysis.md, technical_context_analysis.md
- Perform: System architecture, component relationships, data flows, interfaces
- Create: /architecture/technical_architecture_analysis.md

**PHASE 4 - DETAILED SPECIFICATION (6 Parallel Sub-Agents):**

**Functional Specification Sub-Agent:**
- Read: functional_requirements_analysis.md, user_analysis.md, document_architecture_analysis.md
- Perform: Detailed feature descriptions, user stories, acceptance criteria, workflows
- Create: /specification/functional_specification_analysis.md

**Technical Specification Sub-Agent:**
- Read: technical_architecture_analysis.md, technical_requirements_analysis.md
- Perform: System design, API definitions, data models, architecture diagrams
- Create: /specification/technical_specification_analysis.md

**Interface Specification Sub-Agent:**
- Read: user_analysis.md, functional_specification_analysis.md
- Perform: UI/UX requirements, wireframes, interaction patterns, design guidelines
- Create: /specification/interface_specification_analysis.md

**Integration Specification Sub-Agent:**
- Read: technical_context_analysis.md, technical_specification_analysis.md
- Perform: External system interfaces, data exchange, communication protocols
- Create: /specification/integration_specification_analysis.md

**Testing Specification Sub-Agent:**
- Read: functional_requirements_analysis.md, non_functional_requirements_analysis.md
- Perform: Test strategies, test cases, quality assurance criteria, validation methods
- Create: /specification/testing_specification_analysis.md

**Implementation Specification Sub-Agent:**
- Read: technical_specification_analysis.md, business_requirements_analysis.md
- Perform: Development guidelines, coding standards, deployment procedures
- Create: /specification/implementation_specification_analysis.md

**PHASE 5 - VALIDATION & REFINEMENT (4 Sequential Sub-Agents):**

**DRAFT REVIEW**: Present specification draft to user for feedback

**Completeness Review Sub-Agent:**
- Read: All specification/ documents
- Perform: Verify all requirements covered, identify gaps, ensure consistency
- Create: /validation/completeness_review_analysis.md

**Feasibility Validation Sub-Agent:**
- Read: technical_specification_analysis.md, business_requirements_analysis.md, completeness_review_analysis.md
- Perform: Assess technical feasibility, resource requirements, timeline realism
- Create: /validation/feasibility_validation_analysis.md

**Stakeholder Alignment Sub-Agent:**
- Read: business_context_analysis.md, user_analysis.md, feasibility_validation_analysis.md
- Perform: Validate against business objectives, user needs, technical constraints
- Create: /validation/stakeholder_alignment_analysis.md

**Documentation Quality Sub-Agent:**
- Read: All documents from all phases
- Perform: Review clarity, completeness, usability, maintainability
- Create: /validation/documentation_quality_analysis.md

**Document Template:**

"""markdown
# [Domain] Specification Analysis
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Specification Focus:** [Domain]

## Executive Summary
[Brief overview]

## Detailed Specification Analysis
[Comprehensive analysis]

## Key Requirements
[Specific requirements identified]

## Success Criteria
[Measurable indicators]

## Integration Points
[Cross-domain relationships]

## Implementation Guidance
[Next phase requirements]

## Quality Considerations
[Standards and validation criteria]
"""

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

**Options:** [USER GOAL DESCRIPTION] using [DOCUMENT_DIRECTORY] [OPTIONAL: INTERACTIVE DIALOG | AUTONOMOUS | WITH CHECKPOINTS | REVIEW SPECIFICATION]
```

## Key Benefits
- **Adaptive Dialog Documentation**: Complete record of clarification process and decision rationale
- **Interactive Refinement Tracking**: Full documentation of user feedback and specification evolution
- **Comprehensive Specification Archive**: Detailed preservation of all analysis and specification work
- **Decision Traceability**: Clear documentation of requirements gathering and validation decisions

## Usage
Replace `[USER GOAL DESCRIPTION]` with your goal or project. The workflow will automatically assess clarity and either ask clarifying questions or proceed with specification creation. All interactions and decisions are documented in the specified directory structure.
