# Fix Bugs in Unfamiliar Codebases with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to fix [BUG DESCRIPTION] in unfamiliar codebase. Store findings in [DOCUMENT_DIRECTORY]. Follow this file-based bug fixing workflow:

**PHASE 0 - BUG CLASSIFICATION:**
1. Create directories: /investigation/, /root_cause/, /implementation/, /verification/
2. Analyze bug type, evidence, scope, urgency
3. Create: [DOCUMENT_DIRECTORY]/bug_analysis.md
4. Select investigation strategy based on evidence

**PHASE 1A - ERROR-DRIVEN INVESTIGATION (3 Parallel Sub-Agents):**
**Error Trace Sub-Agent:**
- Read: bug_analysis.md
- Perform: Error point analysis, stack trace components, failure conditions
- Create: /investigation/error_trace_analysis.md

**Call Flow Sub-Agent:**
- Read: bug_analysis.md
- Perform: Execution flow analysis, call stack, data transitions
- Create: /investigation/call_flow_analysis.md

**Data State Sub-Agent:**
- Read: bug_analysis.md
- Perform: Data condition analysis, variable states at failure
- Create: /investigation/data_state_analysis.md

**PHASE 1B - SYMPTOM-DRIVEN INVESTIGATION (3 Parallel Sub-Agents):**
**Reproduction Sub-Agent:**
- Read: bug_analysis.md
- Perform: Systematic reproduction, exact failure point, minimal case
- Create: /investigation/reproduction_analysis.md

**Behavior Comparison Sub-Agent:**
- Read: bug_analysis.md
- Perform: Expected vs actual analysis, deviation points
- Create: /investigation/behavior_comparison_analysis.md

**Logic Flow Sub-Agent:**
- Read: bug_analysis.md
- Perform: Logic trace analysis, where logic diverges
- Create: /investigation/logic_flow_analysis.md

**PHASE 1C - TEST-FAILURE-DRIVEN INVESTIGATION (3 Parallel Sub-Agents):**
**Test Analysis Sub-Agent:**
- Read: bug_analysis.md
- Perform: Test case analysis, expectations, coverage gaps
- Create: /investigation/test_analysis.md

**Test Debugging Sub-Agent:**
- Read: bug_analysis.md
- Perform: Test path debugging, execution flow
- Create: /investigation/test_debugging_analysis.md

**Regression Analysis Sub-Agent:**
- Read: bug_analysis.md
- Perform: Change regression analysis, impact assessment
- Create: /investigation/regression_analysis.md

**PHASE 2 - ROOT CAUSE ANALYSIS (1 Sub-Agent):**
- Read: All investigation/ documents
- Perform: Bottom-up analysis, root cause identification, fix planning
- Create: /root_cause/root_cause_analysis.md

**PHASE 3 - IMPLEMENTATION (1 Sub-Agent):**
- Read: root_cause_analysis.md
- Perform: Surgical fix implementation, minimal changes, test updates
- Create: /implementation/fix_implementation.md

**PHASE 4 - VERIFICATION (3 Sequential Sub-Agents):**

**Bug Resolution Verification Sub-Agent:**
- Read: bug_analysis.md, fix_implementation.md
- Perform: Original bug verification using reproduction steps
- Create: /verification/bug_resolution_verification.md

**Regression Testing Sub-Agent:**
- Read: fix_implementation.md, bug_resolution_verification.md
- Perform: Comprehensive regression testing
- Create: /verification/regression_testing.md

**Edge Case Testing Sub-Agent:**
- Read: root_cause_analysis.md, regression_testing.md
- Perform: Edge cases and boundary conditions testing
- Create: /verification/edge_case_testing.md

**Document Template:**

"""markdown
# [Domain] Bug Analysis/Implementation
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Bug Context:** [Brief description]

## Executive Summary
[Brief overview]

## Detailed Analysis/Implementation
[Comprehensive findings or code changes]

## Evidence/Code Changes
[Supporting evidence or modifications]

## Integration Points
[Component relationships]

## Next Phase Requirements
[Guidance for next phase]

## Issues/Conflicts
[Problems identified]
"""

**Investigation Scope:**
- Investigation sub-agents follow bottom-up approach
- Sub-agents focus on assigned aspect only
- No fixes during investigation - evidence gathering only
- Complete analysis before documenting

**Options:** [BUG DESCRIPTION] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW INVESTIGATION | REVIEW FIX]
```

## Key Benefits
- **Complete Investigation Trail**: Detailed documentation of all analysis steps
- **Evidence Preservation**: Stack traces, reproduction steps fully documented
- **Root Cause Clarity**: Clear trail from symptoms to fix
- **Knowledge Building**: Bug patterns captured for future reference
