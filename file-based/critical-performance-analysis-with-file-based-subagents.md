# How to Perform Critical Performance Analysis Using File-Based Sub-Agent Communication

## Overview
This workflow provides comprehensive performance analysis for code changes with the rigor expected in game engines, graphics engines, and critical systems where speed, space efficiency, reliability, and robustness are paramount. Each analysis phase creates detailed documentation, ensuring thorough performance evaluation and optimization guidance.

## Complete Critical Performance Analysis Workflow Prompt

```
I need to perform critical performance analysis for [CODE CHANGE DESCRIPTION] in [REPOSITORY/BRANCH]. Store all sub-agent findings in [DOCUMENT_DIRECTORY]. This analysis must meet the standards of game engines, graphics engines, and critical systems where performance is paramount. Follow this file-based performance analysis workflow:

**PHASE 0 - PERFORMANCE SCOPE ASSESSMENT (Main Agent):**
1. Create document directory structure in [DOCUMENT_DIRECTORY]:
   - /phase_1_domain_analysis/
   - /phase_2_integration_analysis/
   - /phase_3_optimization_recommendations/
   - /phase_4_implementation_guidance/
2. Check existing knowledge graph for performance patterns and previous optimization work
3. Analyze code changes to identify performance-critical areas: algorithms, data structures, memory access patterns, I/O operations
4. Determine baseline performance requirements and acceptable performance budgets
5. Create initial todo breakdown using todo_write with performance priorities
6. Create: [DOCUMENT_DIRECTORY]/performance_scope.md (documenting performance requirements and critical areas)

**PHASE 1 - MULTI-DOMAIN PERFORMANCE ANALYSIS (6 Parallel Sub-Agents):**
7. Deploy SIX parallel sub-agents simultaneously for comprehensive performance domain coverage:

   **Algorithm Performance Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/performance_scope.md
   - Perform: Algorithm performance analysis - analyze time complexity (Big-O), space complexity, algorithmic efficiency, optimization opportunities, loop structures, recursive patterns
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/algorithm_performance_analysis.md (documenting completed algorithm analysis)

   **Data Structure Performance Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/performance_scope.md
   - Perform: Data structure performance analysis - evaluate data structure choices, access patterns, cache efficiency, memory layout optimization, data locality
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/data_structure_performance_analysis.md (documenting completed data structure analysis)

   **Memory Performance Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/performance_scope.md
   - Perform: Memory performance analysis - analyze memory allocation patterns, garbage collection impact, memory fragmentation, resource lifecycle management
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/memory_performance_analysis.md (documenting completed memory analysis)

   **I/O Performance Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/performance_scope.md
   - Perform: I/O performance analysis - evaluate file system operations, network I/O, database queries, I/O blocking patterns, asynchronous operations
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/io_performance_analysis.md (documenting completed I/O analysis)

   **Concurrency Performance Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/performance_scope.md
   - Perform: Concurrency performance analysis - analyze thread safety, lock contention, parallel processing efficiency, synchronization overhead
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/concurrency_performance_analysis.md (documenting completed concurrency analysis)

   **System Resource Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/performance_scope.md
   - Perform: System resource analysis - evaluate CPU utilization, memory bandwidth, cache miss rates, system call overhead, hardware efficiency
   - Create: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/system_resource_analysis.md (documenting completed system analysis)

8. Main Agent: Read all domain performance documents, check for contradictions
9. **IF CONTRADICTIONS FOUND**: Repeat Phase 1 with clarified scope and specific conflict resolution instructions
10. **CHECKPOINT 1**: If checkpoints enabled, present performance domain analysis and critical issue identification

**PHASE 2 - PERFORMANCE INTEGRATION ANALYSIS (1 Sub-Agent):**
11. Deploy ONE sub-agent for integration analysis:
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/
    - Perform: Performance integration analysis - analyze performance trade-offs between different optimizations, system-level performance interactions, end-to-end performance impact assessment
    - Create: [DOCUMENT_DIRECTORY]/phase_2_integration_analysis/performance_integration_analysis.md (documenting completed integration analysis)

12. Main Agent: Read integration analysis, validate findings
13. **IF CONFLICTS WITH DOMAIN ANALYSIS**: Repeat relevant Phase 1 sub-agents with integration context
14. **CHECKPOINT 2**: If checkpoints enabled, present integrated performance analysis and optimization strategy

**PHASE 3 - PERFORMANCE OPTIMIZATION RECOMMENDATIONS (4 Parallel Sub-Agents):**
15. Deploy FOUR parallel sub-agents for optimization strategy development:

    **Critical Bottleneck Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/algorithm_performance_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/memory_performance_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_integration_analysis/performance_integration_analysis.md
    - Perform: Critical bottleneck analysis - identify performance-blocking issues requiring immediate attention, deployment blockers, critical path optimizations
    - Create: [DOCUMENT_DIRECTORY]/phase_3_optimization_recommendations/critical_bottleneck_analysis.md (documenting bottleneck analysis)

    **Space-Time Optimization Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/algorithm_performance_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/data_structure_performance_analysis.md
    - Perform: Space-time optimization analysis - recommend space-time trade-offs, memory vs CPU optimizations, algorithmic improvements
    - Create: [DOCUMENT_DIRECTORY]/phase_3_optimization_recommendations/space_time_optimization_analysis.md (documenting optimization analysis)

    **Scalability Enhancement Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/concurrency_performance_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/system_resource_analysis.md
    - Perform: Scalability enhancement analysis - assess performance under load, concurrent access patterns, scalability bottlenecks
    - Create: [DOCUMENT_DIRECTORY]/phase_3_optimization_recommendations/scalability_enhancement_analysis.md (documenting scalability analysis)

    **Performance Future-Proofing Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_integration_analysis/performance_integration_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_domain_analysis/system_resource_analysis.md
    - Perform: Performance future-proofing analysis - assess long-term performance sustainability, technical debt implications, maintenance overhead
    - Create: [DOCUMENT_DIRECTORY]/phase_3_optimization_recommendations/performance_future_proofing_analysis.md (documenting future-proofing analysis)

16. Main Agent: Read all optimization documents, resolve conflicts
17. **IF OPTIMIZATION CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
18. **CHECKPOINT 3**: If checkpoints enabled, review optimization recommendations before implementation guidance

**PHASE 4 - IMPLEMENTATION GUIDANCE (3 Sequential Sub-Agents):**
19. Deploy THREE sub-agents sequentially for implementation guidance:

    **Optimization Priority Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_optimization_recommendations/critical_bottleneck_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_optimization_recommendations/space_time_optimization_analysis.md
    - Perform: Optimization prioritization - create prioritized optimization roadmap with impact assessment, effort estimation
    - Create: [DOCUMENT_DIRECTORY]/phase_4_implementation_guidance/optimization_priority_analysis.md (documenting priority analysis)

    **Implementation Strategy Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_4_implementation_guidance/optimization_priority_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_optimization_recommendations/scalability_enhancement_analysis.md
    - Perform: Implementation strategy development - provide specific implementation guidance, code examples, performance testing approaches
    - Create: [DOCUMENT_DIRECTORY]/phase_4_implementation_guidance/implementation_strategy_analysis.md (documenting strategy analysis)

    **Performance Monitoring Sub-Agent:**
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_3_optimization_recommendations/
    - Perform: Performance monitoring design - create performance monitoring strategy, benchmarking approaches, regression detection
    - Create: [DOCUMENT_DIRECTORY]/phase_4_implementation_guidance/performance_monitoring_analysis.md (documenting monitoring analysis)

20. Main Agent: Compile final performance analysis report from all phase documents

**DOCUMENT STRUCTURE REQUIREMENTS:**

Each sub-agent document must include:

"""markdown
# [Domain] Performance Analysis
**Agent:** [Sub-Agent Name]
**Phase:** [Phase Number]
**Timestamp:** [ISO Timestamp]
**Documents Read:** [List of input documents]
**Performance Focus:** [Specific performance domain]

## Executive Summary
[Brief overview of performance analysis completed]

## Detailed Performance Findings
[Comprehensive analysis within performance domain]

## Performance Metrics and Benchmarks
[Quantitative performance data and measurements]

## Optimization Opportunities
[Specific improvement recommendations]

## Performance Risks
[Performance-related risks and concerns]

## Integration Points
[How findings relate to other performance domains]

## Implementation Considerations
[Practical guidance for performance improvements]
"""

**PERFORMANCE ANALYSIS SCOPE ISOLATION:**
- **Domain sub-agents focus exclusively on their performance area** without attempting system-wide optimization recommendations
- **Integration analysis happens only in designated integration phase** after domain analysis completion
- **Optimization sub-agents work within their specialization** without overlapping into other optimization areas
- **Implementation guidance sub-agents provide practical guidance** without modifying strategic direction
- **Main agent maintains performance oversight** and handles all integration and strategic decisions

**CONFLICT RESOLUTION PROTOCOL:**
1. Main Agent identifies contradictions between performance documents
2. Create performance_conflict_resolution_[timestamp].md documenting specific conflicts
3. Re-run affected sub-agents with conflict context and additional guidance
4. Continue workflow with updated documents

**PERFORMANCE STANDARDS:**
- **Quantitative Analysis**: All performance conclusions supported by measurable data and benchmarks
- **Critical System Requirements**: Analysis meets standards for real-time, safety-critical, and high-performance systems
- **Optimization Validation**: Performance improvements verified through testing and measurement
- **Scalability Assessment**: Performance evaluated under various load conditions and usage patterns

**HUMAN FEEDBACK OPTIONS:**
- **Default**: Fully autonomous execution with comprehensive performance analysis report
- **Add "WITH CHECKPOINTS"**: Pause after each major phase for review and guidance
- **Add "REVIEW DOMAIN_ANALYSIS"**: Pause only after Phase 1 to confirm performance domain findings
- **Add "REVIEW OPTIMIZATION"**: Pause only after Phase 3 to review optimization recommendations

**CODE CHANGES TO ANALYZE:**
[CODE CHANGE DESCRIPTION] in [REPOSITORY/BRANCH] using document directory [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW DOMAIN_ANALYSIS | REVIEW OPTIMIZATION]

Begin with Phase 0 performance scope assessment and proceed systematically through each phase with comprehensive performance evaluation.
```

## Usage Instructions

1. **Replace placeholders** with specific information:
   - `[CODE CHANGE DESCRIPTION]` - Detailed description of code changes requiring performance analysis
   - `[REPOSITORY/BRANCH]` - Specific repository and branch being analyzed
   - `[DOCUMENT_DIRECTORY]` - Absolute path where documents should be stored (e.g., "/project/performance/auth-optimization")

2. **Prepare document directory** - Ensure the specified directory exists and is writable

3. **Choose feedback level** by adding optional modifiers for human checkpoints

## Key Benefits of File-Based Communication

- **Comprehensive Performance Documentation**: Complete preservation of all performance analysis findings
- **Quantitative Data Preservation**: Performance metrics and benchmarks maintained for future reference
- **Optimization Traceability**: Clear trail from performance issues to optimization recommendations
- **Cross-Domain Analysis**: Systematic integration of performance findings across multiple domains
- **Implementation Guidance**: Detailed documentation for performance optimization implementation
- **Knowledge Building**: Performance patterns and optimization techniques captured for future projects

## Document Organization Example

```
/project/performance/auth-optimization/
├── performance_scope.md
├── phase_1_domain_analysis/
│   ├── algorithm_performance_analysis.md
│   ├── data_structure_performance_analysis.md
│   ├── memory_performance_analysis.md
│   ├── io_performance_analysis.md
│   ├── concurrency_performance_analysis.md
│   └── system_resource_analysis.md
├── phase_2_integration_analysis/
│   └── performance_integration_analysis.md
├── phase_3_optimization_recommendations/
│   ├── critical_bottleneck_analysis.md
│   ├── space_time_optimization_analysis.md
│   ├── scalability_enhancement_analysis.md
│   └── performance_future_proofing_analysis.md
└── phase_4_implementation_guidance/
    ├── optimization_priority_analysis.md
    ├── implementation_strategy_analysis.md
    └── performance_monitoring_analysis.md
```

## Performance Analysis Domains

**Algorithm Performance Focus:**
- Time complexity (Big-O) analysis and verification
- Space complexity assessment and optimization
- Loop optimization and recursive algorithm improvements
- Algorithmic efficiency and alternative algorithm evaluation

**Data Structure Performance Focus:**
- Cache locality and memory access pattern optimization
- Data structure choice evaluation and recommendations
- Memory layout optimization for performance
- Access pattern analysis and efficiency improvements

**Memory Performance Focus:**
- Memory allocation pattern analysis and optimization
- Garbage collection impact assessment and mitigation
- Memory fragmentation analysis and prevention
- Resource lifecycle management and memory efficiency

**I/O Performance Focus:**
- File system operation optimization and analysis
- Network I/O performance evaluation and improvement
- Database query performance analysis and optimization
- Asynchronous I/O implementation and blocking pattern analysis

**Concurrency Performance Focus:**
- Thread safety analysis and lock contention evaluation
- Parallel processing efficiency assessment and optimization
- Synchronization overhead analysis and reduction
- Lock-free algorithm evaluation and implementation guidance

**System Resource Focus:**
- CPU utilization analysis and optimization opportunities
- Memory bandwidth assessment and cache efficiency
- System call overhead evaluation and reduction
- Hardware efficiency and resource utilization optimization

## Advanced Performance Features

- **Nested Analysis Capability**: Deep dive analysis for critical performance bottlenecks
- **Cross-Domain Optimization**: Integration analysis prevents optimization conflicts
- **Quantitative Validation**: Performance improvements verified through measurement
- **Scalability Assessment**: Performance evaluated under various load conditions
- **Future-Proofing**: Long-term performance sustainability and maintenance considerations
- **Implementation Guidance**: Practical code examples and optimization strategies
