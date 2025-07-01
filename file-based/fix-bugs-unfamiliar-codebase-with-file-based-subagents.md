# How to Fix Bugs in Unfamiliar Codebases Using File-Based Sub-Agent Communication

## Overview
This adaptive workflow systematically diagnoses and fixes bugs in unknown codebases by using strategic sub-agent delegation with persistent file-based communication. Each investigation phase creates detailed documentation, ensuring comprehensive analysis and reliable fixes.

## Complete Bug Fixing Workflow Prompt

```
I need to fix [BUG DESCRIPTION] in this unfamiliar codebase. Store all sub-agent findings in [DOCUMENT_DIRECTORY]. Follow this file-based bug fixing workflow:

**PHASE 0 - BUG CLASSIFICATION & CONTEXT (Main Agent):**
1. Create document directory structure in [DOCUMENT_DIRECTORY]:
   - /phase_1_investigation/
   - /phase_2_root_cause/
   - /phase_3_implementation/
   - /phase_4_verification/
2. Check existing knowledge graph for this codebase and related bug patterns
3. Analyze the bug report to determine:
   - **Bug Type**: Crash, logic error, performance, UI issue, integration failure, data corruption, etc.
   - **Available Evidence**: Error messages, stack traces, reproduction steps, failing tests, user reports
   - **Scope Indicators**: Single component, multi-component, system-wide impact
   - **Urgency Level**: Critical system failure, feature malfunction, edge case issue
4. Create initial todo breakdown using todo_write
5. Create: [DOCUMENT_DIRECTORY]/bug_analysis.md (documenting bug classification and evidence)
6. Select appropriate investigation strategy based on available evidence

**PHASE 1A - ERROR-DRIVEN INVESTIGATION (3 Parallel Sub-Agents):**
7. Deploy THREE parallel sub-agents simultaneously:

   **Error Trace Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
   - Perform: Error point analysis - start from exact error location and trace backwards, analyze stack trace components, identify immediate failure conditions
   - Create: [DOCUMENT_DIRECTORY]/phase_1_investigation/error_trace_analysis.md (documenting completed error tracing)

   **Call Flow Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
   - Perform: Execution flow analysis - analyze call stack and execution path leading to error, map function calls and data transitions
   - Create: [DOCUMENT_DIRECTORY]/phase_1_investigation/call_flow_analysis.md (documenting completed flow analysis)

   **Data State Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
   - Perform: Data condition analysis - investigate data/state conditions that triggered problematic code path, analyze variable states at failure point
   - Create: [DOCUMENT_DIRECTORY]/phase_1_investigation/data_state_analysis.md (documenting completed data analysis)

8. Main Agent: Read all investigation documents, synthesize findings to identify root cause vs symptoms
9. **CHECKPOINT 1**: If checkpoints enabled, present investigation findings and root cause hypothesis

**PHASE 1B - SYMPTOM-DRIVEN INVESTIGATION (3 Parallel Sub-Agents):**
10. Deploy THREE parallel sub-agents simultaneously:

    **Reproduction Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
    - Perform: Systematic reproduction - reproduce issue step-by-step, identify exact failure point, document minimal reproduction case
    - Create: [DOCUMENT_DIRECTORY]/phase_1_investigation/reproduction_analysis.md (documenting completed reproduction work)

    **Behavior Comparison Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
    - Perform: Expected vs actual analysis - compare expected vs actual behavior in failing component areas, identify deviation points
    - Create: [DOCUMENT_DIRECTORY]/phase_1_investigation/behavior_comparison_analysis.md (documenting completed behavior analysis)

    **Logic Flow Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
    - Perform: Logic trace analysis - trace data flow and logic that should produce correct behavior, identify where logic diverges
    - Create: [DOCUMENT_DIRECTORY]/phase_1_investigation/logic_flow_analysis.md (documenting completed logic analysis)

11. Main Agent: Read all investigation documents, synthesize findings to identify where logic diverges from expectations
12. **CHECKPOINT 1**: If checkpoints enabled, present reproduction results and failure analysis

**PHASE 1C - TEST-FAILURE-DRIVEN INVESTIGATION (3 Parallel Sub-Agents):**
13. Deploy THREE parallel sub-agents simultaneously:

    **Test Analysis Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
    - Perform: Test case analysis - analyze failing test cases and their expectations in detail, understand test coverage gaps
    - Create: [DOCUMENT_DIRECTORY]/phase_1_investigation/test_analysis.md (documenting completed test analysis)

    **Test Debugging Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
    - Perform: Test path debugging - debug exact code path that failing tests exercise, identify test execution flow
    - Create: [DOCUMENT_DIRECTORY]/phase_1_investigation/test_debugging_analysis.md (documenting completed test debugging)

    **Regression Analysis Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
    - Perform: Change regression analysis - identify recent changes or conditions that broke tested functionality, analyze change impact
    - Create: [DOCUMENT_DIRECTORY]/phase_1_investigation/regression_analysis.md (documenting completed regression analysis)

14. Main Agent: Read all investigation documents, synthesize findings to pinpoint regression cause
15. **CHECKPOINT 1**: If checkpoints enabled, present test analysis and regression findings

**PHASE 2 - ROOT CAUSE IDENTIFICATION & SOLUTION PLANNING (Single Sub-Agent):**
16. Deploy ONE specialized sub-agent for root cause analysis:
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_1_investigation/
    - Perform: Root cause analysis - apply bottom-up principle starting from lowest-level failure, trace impact upward, map component boundaries for multi-component issues, plan minimal targeted fix approach addressing root cause, identify affected areas and side effects, create comprehensive test strategy
    - Create: [DOCUMENT_DIRECTORY]/phase_2_root_cause/root_cause_analysis.md (documenting completed root cause analysis and fix planning)

17. Main Agent: Read root cause analysis, validate fix approach, update todos
18. **CHECKPOINT 2**: If checkpoints enabled, present root cause analysis and fix strategy

**PHASE 3 - TARGETED IMPLEMENTATION (Single Sub-Agent):**
19. Deploy ONE focused sub-agent for implementation:
    - Read: [DOCUMENT_DIRECTORY]/phase_2_root_cause/root_cause_analysis.md
    - Perform: Surgical fix implementation - fix identified root cause with minimal code changes, follow existing code patterns and error handling, implement/update tests specifically for bug scenario
    - Create: [DOCUMENT_DIRECTORY]/phase_3_implementation/fix_implementation.md (documenting completed fix implementation)

20. Main Agent: Track progress, update todos, store bug pattern knowledge
21. **CHECKPOINT 3**: If checkpoints enabled, review implemented fix before verification

**PHASE 4 - COMPREHENSIVE VERIFICATION (Sequential Sub-Agents):**
22. Deploy THREE sub-agents sequentially:

    **Bug Resolution Verification Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/bug_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_implementation/fix_implementation.md
    - Perform: Original bug verification - verify original bug is completely resolved using reproduction steps, test all reported scenarios
    - Create: [DOCUMENT_DIRECTORY]/phase_4_verification/bug_resolution_verification.md (documenting verification results)

    **Regression Testing Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_implementation/fix_implementation.md
    - Read: [DOCUMENT_DIRECTORY]/phase_4_verification/bug_resolution_verification.md
    - Perform: Regression testing - run comprehensive regression testing to ensure no new issues introduced, validate related functionality
    - Create: [DOCUMENT_DIRECTORY]/phase_4_verification/regression_testing.md (documenting regression test results)

    **Edge Case Testing Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_root_cause/root_cause_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_4_verification/regression_testing.md
    - Perform: Edge case testing - test edge cases and boundary conditions around fix area, validate fix robustness
    - Create: [DOCUMENT_DIRECTORY]/phase_4_verification/edge_case_testing.md (documenting edge case test results)

23. Main Agent: Handle any verification failures, update knowledge graph with bug patterns and solutions

**DOCUMENT STRUCTURE REQUIREMENTS:**

Each sub-agent document must include:
```markdown
# [Domain] Analysis/Implementation
**Agent:** [Sub-Agent Name]
**Phase:** [Phase Number]
**Timestamp:** [ISO Timestamp]
**Documents Read:** [List of input documents]
**Bug Context:** [Brief bug description]

## Executive Summary
[Brief overview of work completed]

## Detailed Analysis/Implementation
[Comprehensive investigation findings or implementation details]

## Evidence/Code Changes
[Supporting evidence, stack traces, or code modifications]

## Integration Points
[How findings relate to other components/analysis]

## Next Phase Requirements
[What subsequent phases need to know]

## Issues/Conflicts
[Any problems or contradictions identified]
```

**INVESTIGATION SCOPE ISOLATION:**
- **Investigation sub-agents follow bottom-up approach** - start from failure point and work backwards
- **Each investigation sub-agent focuses on assigned aspect** (error tracing, reproduction, data analysis)
- **Sub-agents must NOT attempt fixes during investigation** - only gather and analyze evidence
- **Sub-agents IGNORE unrelated issues** unless directly connected to the bug
- **Complete analysis before documenting findings**

**IMPLEMENTATION PHASE ISOLATION:**
- **Implementation sub-agent modifies ONLY code related to identified root cause**
- **Must NOT run global checks during implementation** (same rules as feature development)
- **Focus on minimal, surgical changes** rather than broad refactoring
- **Validate changes only against specific bug scenario**, not entire codebase

**CONFLICT RESOLUTION PROTOCOL:**
1. Main Agent identifies contradictions between investigation documents
2. Create conflict_resolution_[timestamp].md documenting specific conflicts
3. Re-run affected sub-agents with conflict context and additional guidance
4. Continue workflow with updated documents

**HUMAN FEEDBACK OPTIONS:**
- **Default**: Fully autonomous execution with final summary
- **Add "WITH CHECKPOINTS"**: Pause after each major phase for review and approval
- **Add "REVIEW INVESTIGATION"**: Pause only after Phase 1 to confirm root cause before fixing
- **Add "REVIEW FIX"**: Pause only after Phase 3 to review implemented solution before verification

**BUG TO FIX:**
[BUG DESCRIPTION] using document directory [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW INVESTIGATION | REVIEW FIX]

Begin with Phase 0 bug classification and proceed with the appropriate investigation strategy based on available evidence.
```

## Usage Instructions

1. **Replace placeholders** with specific information:
   - `[BUG DESCRIPTION]` - Detailed description including symptoms, error messages, reproduction steps, expected vs actual behavior, environment details
   - `[DOCUMENT_DIRECTORY]` - Absolute path where documents should be stored (e.g., "/project/bugs/user-auth-failure")

2. **Prepare document directory** - Ensure the specified directory exists and is writable

3. **Choose feedback level** by adding optional modifiers for human checkpoints

4. **The workflow automatically adapts** based on available evidence:
   - Error messages/stack traces → Error-driven investigation (Phase 1A)
   - Behavioral issues → Symptom-driven investigation (Phase 1B)
   - Test failures → Test-failure-driven investigation (Phase 1C)

## Key Benefits of File-Based Communication

- **Complete Investigation Trail**: Detailed documentation of all analysis steps and findings
- **Evidence Preservation**: Stack traces, reproduction steps, and data states fully documented
- **Systematic Analysis**: Each investigation aspect thoroughly documented for review
- **Root Cause Clarity**: Clear documentation trail from symptoms to root cause to fix
- **Knowledge Building**: Bug patterns and debugging techniques captured for future reference
- **Verification Completeness**: Comprehensive testing documentation ensures thorough validation

## Document Organization Example

```
/project/bugs/user-auth-failure/
├── bug_analysis.md
├── phase_1_investigation/
│   ├── error_trace_analysis.md
│   ├── call_flow_analysis.md
│   └── data_state_analysis.md
├── phase_2_root_cause/
│   └── root_cause_analysis.md
├── phase_3_implementation/
│   └── fix_implementation.md
└── phase_4_verification/
    ├── bug_resolution_verification.md
    ├── regression_testing.md
    └── edge_case_testing.md
```

## Investigation Strategy Selection

**Error-Driven (Phase 1A)** - Use when you have:
- Stack traces
- Exception messages  
- Crash logs
- Runtime errors

**Symptom-Driven (Phase 1B)** - Use when you have:
- User behavior reports
- Incorrect outputs
- UI/UX issues
- Performance problems

**Test-Failure-Driven (Phase 1C)** - Use when you have:
- Failing unit/integration tests
- CI/CD pipeline failures
- Regression after changes

## Advanced Features

- **Pattern Recognition**: Documents enable identification of recurring bug patterns
- **Knowledge Reuse**: Previous bug fixes inform similar future issues
- **Comprehensive Audit**: Complete trail from initial report to verified fix
- **Team Learning**: Debugging techniques and patterns shared across projects
- **Quality Assurance**: Systematic verification ensures reliable fixes

## Common Pitfalls Avoided

- **Information Loss**: Complete investigation findings preserved in structured documents
- **Symptom Fixes**: Root cause analysis documents prevent surface-level fixes
- **Regression Risk**: Comprehensive verification documents ensure thorough testing
- **Context Loss**: Detailed documentation maintains continuity between phases
- **Investigation Overlap**: Clear phase separation prevents redundant analysis
- **Fix Validation**: Systematic verification ensures fixes work without side effects
