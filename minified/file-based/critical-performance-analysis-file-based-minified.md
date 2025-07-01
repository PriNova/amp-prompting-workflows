# Critical Performance Analysis with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need critical performance analysis for [CODE CHANGE DESCRIPTION] in [REPOSITORY/BRANCH]. Store findings in [DOCUMENT_DIRECTORY]. Must meet game engine/graphics engine standards. Follow this file-based performance workflow:

**PHASE 0 - PERFORMANCE SCOPE:**
1. Create directories: /domain_analysis/, /integration_analysis/, /optimization/, /implementation/
2. Identify performance-critical areas, baseline requirements, hot paths
3. Create: [DOCUMENT_DIRECTORY]/performance_scope.md

**PHASE 1 - DOMAIN ANALYSIS (6 Parallel Sub-Agents):**

**Algorithm Performance Sub-Agent:**
- Read: performance_scope.md
- Perform: Time/space complexity, algorithmic efficiency, optimization opportunities
- Create: /domain_analysis/algorithm_performance_analysis.md

**Data Structure Performance Sub-Agent:**
- Read: performance_scope.md
- Perform: Data structure choices, cache efficiency, memory layout optimization
- Create: /domain_analysis/data_structure_performance_analysis.md

**Memory Performance Sub-Agent:**
- Read: performance_scope.md
- Perform: Allocation patterns, GC impact, fragmentation, resource lifecycle
- Create: /domain_analysis/memory_performance_analysis.md

**I/O Performance Sub-Agent:**
- Read: performance_scope.md
- Perform: File/network operations, I/O blocking patterns, async operations
- Create: /domain_analysis/io_performance_analysis.md

**Concurrency Performance Sub-Agent:**
- Read: performance_scope.md
- Perform: Thread safety, lock contention, parallel processing efficiency
- Create: /domain_analysis/concurrency_performance_analysis.md

**System Resource Sub-Agent:**
- Read: performance_scope.md
- Perform: CPU utilization, memory bandwidth, cache miss rates, system calls
- Create: /domain_analysis/system_resource_analysis.md

**PHASE 2 - INTEGRATION ANALYSIS (1 Sub-Agent):**
- Read: All domain_analysis/ documents
- Perform: Performance trade-offs, system-level interactions, end-to-end impact
- Create: /integration_analysis/performance_integration_analysis.md

**PHASE 3 - OPTIMIZATION RECOMMENDATIONS (4 Parallel Sub-Agents):**

**Critical Bottleneck Sub-Agent:**
- Read: algorithm_performance_analysis.md, memory_performance_analysis.md, performance_integration_analysis.md
- Perform: Performance blockers, deployment blockers, critical path optimization
- Create: /optimization/critical_bottleneck_analysis.md

**Space-Time Optimization Sub-Agent:**
- Read: algorithm_performance_analysis.md, data_structure_performance_analysis.md
- Perform: Space-time trade-offs, memory vs CPU optimization, algorithmic improvements
- Create: /optimization/space_time_optimization_analysis.md

**Scalability Enhancement Sub-Agent:**
- Read: concurrency_performance_analysis.md, system_resource_analysis.md
- Perform: Performance under load, concurrent access patterns, scalability bottlenecks
- Create: /optimization/scalability_enhancement_analysis.md

**Performance Future-Proofing Sub-Agent:**
- Read: performance_integration_analysis.md, system_resource_analysis.md
- Perform: Long-term sustainability, technical debt, maintenance overhead
- Create: /optimization/performance_future_proofing_analysis.md

**PHASE 4 - IMPLEMENTATION GUIDANCE (3 Sequential Sub-Agents):**

**Optimization Priority Sub-Agent:**
- Read: critical_bottleneck_analysis.md, space_time_optimization_analysis.md
- Perform: Prioritized optimization roadmap, impact assessment, effort estimation
- Create: /implementation/optimization_priority_analysis.md

**Implementation Strategy Sub-Agent:**
- Read: optimization_priority_analysis.md, scalability_enhancement_analysis.md
- Perform: Implementation guidance, code examples, performance testing approaches
- Create: /implementation/implementation_strategy_analysis.md

**Performance Monitoring Sub-Agent:**
- Read: All optimization/ documents
- Perform: Monitoring strategy, benchmarking approaches, regression detection
- Create: /implementation/performance_monitoring_analysis.md

**Document Template:**

"""markdown
# [Domain] Performance Analysis
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Performance Focus:** [Domain]

## Executive Summary
[Brief overview]

## Detailed Performance Findings
[Comprehensive analysis]

## Performance Metrics and Benchmarks
[Quantitative data]

## Optimization Opportunities
[Specific improvements]

## Performance Risks
[Risks and concerns]

## Integration Points
[Cross-domain relationships]

## Implementation Considerations
[Practical guidance]
"""

**Performance Standards:**
- Quantitative analysis with measurable data and benchmarks
- Critical system requirements for real-time/safety-critical systems
- Optimization validation through testing and measurement
- Scalability evaluation under various load conditions

**Options:** [CODE CHANGE DESCRIPTION] in [REPOSITORY/BRANCH] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW DOMAIN_ANALYSIS | REVIEW OPTIMIZATION]
```

## Key Benefits
- **Comprehensive Documentation**: All performance analysis preserved with metrics
- **Quantitative Data Preservation**: Benchmarks maintained for future reference
- **Optimization Traceability**: Clear trail from issues to recommendations
- **Implementation Guidance**: Detailed documentation for performance optimization
