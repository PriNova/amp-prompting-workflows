# Thorough Code Review with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to perform thorough code review for [CODE CHANGE DESCRIPTION] in [REPOSITORY/BRANCH]. Store findings in [DOCUMENT_DIRECTORY]. Follow this file-based review workflow:

**PHASE 0 - SCOPE ASSESSMENT:**
1. Create directories: /domain_analysis/, /integration_analysis/, /recommendations/, /final_report/
2. Analyze code changes scope, complexity, impact areas
3. Create: [DOCUMENT_DIRECTORY]/review_scope.md

**PHASE 1 - DOMAIN ANALYSIS (6 Parallel Sub-Agents):**
Deploy six parallel sub-agents:

**Security Sub-Agent:**
- Read: review_scope.md
- Perform: Security analysis - vulnerabilities, authentication, authorization, data validation
- Create: /domain_analysis/security_findings.md

**Performance Sub-Agent:**
- Read: review_scope.md  
- Perform: Performance analysis - efficiency, optimization, resource usage
- Create: /domain_analysis/performance_findings.md

**Architecture Sub-Agent:**
- Read: review_scope.md
- Perform: Architecture analysis - design patterns, maintainability, scalability
- Create: /domain_analysis/architecture_findings.md

**Testing Sub-Agent:**
- Read: review_scope.md
- Perform: Testing analysis - coverage, quality, edge cases
- Create: /domain_analysis/testing_findings.md

**Functionality Sub-Agent:**
- Read: review_scope.md
- Perform: Functionality analysis - business logic, requirements, UX impact
- Create: /domain_analysis/functionality_findings.md

**Documentation Sub-Agent:**
- Read: review_scope.md
- Perform: Documentation analysis - comments, API docs, clarity
- Create: /domain_analysis/documentation_findings.md

**PHASE 2 - INTEGRATION ANALYSIS (1 Sub-Agent):**
- Read: All domain_analysis/ documents
- Perform: Cross-domain impact analysis, interaction effects, system-wide implications
- Create: /integration_analysis/cross_domain_impact.md

**PHASE 3 - RECOMMENDATIONS (3 Parallel Sub-Agents):**

**Critical Issues Sub-Agent:**
- Read: security_findings.md, performance_findings.md, cross_domain_impact.md
- Perform: Critical issue prioritization, blocking issues, severity assessment
- Create: /recommendations/critical_issues.md

**Improvements Sub-Agent:**
- Read: architecture_findings.md, testing_findings.md, documentation_findings.md
- Perform: Enhancement identification, best practices, optimization opportunities  
- Create: /recommendations/improvements.md

**Future Impact Sub-Agent:**
- Read: architecture_findings.md, cross_domain_impact.md
- Perform: Long-term maintainability, technical debt, architectural implications
- Create: /recommendations/future_impact.md

**PHASE 4 - FINAL REPORT (3 Sequential Sub-Agents):**

**Summary Sub-Agent:**
- Read: critical_issues.md, improvements.md
- Perform: Executive summary creation, key findings synthesis
- Create: /final_report/executive_summary.md

**Action Items Sub-Agent:**
- Read: All recommendations/, executive_summary.md
- Perform: Prioritized action list creation, developer guidance
- Create: /final_report/action_items.md

**Knowledge Sub-Agent:**
- Read: All documents from all phases
- Perform: Pattern extraction, lessons learned documentation
- Create: /final_report/lessons_learned.md

**Document Template:**

"""markdown
# [Domain] Review Findings
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Relevant For:** [Next Phase Agents]

## Executive Summary
[Brief overview]

## Detailed Findings
[Comprehensive analysis]

## Integration Points
[Cross-domain relationships]

## Recommendations
[Domain-specific suggestions]

## Conflicts/Uncertainties
[Issues identified]
"""

**Options:** [CODE CHANGE DESCRIPTION] in [REPOSITORY/BRANCH] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW ANALYSIS | REVIEW RECOMMENDATIONS]
```

## Key Benefits
- **Complete Documentation**: All findings preserved in structured documents
- **Selective Context**: Sub-agents read only relevant documents
- **Conflict Detection**: Systematic document comparison reveals issues
- **Knowledge Building**: Review patterns captured for future use
- **Audit Trail**: Complete record of review process and decisions
