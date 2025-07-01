# Strategic Sub-Agent Orchestration Framework with File-Based Communication (Minified)

## Framework Overview

Systematic approaches for complex projects using file-based sub-agent delegation across three domains: Market Research, Idea Manifestation, and Strategic Planning.

### Core Principles
- **Phase-Based Progression**: Systematic advancement with clear handoffs
- **File-Based Communication**: Document-based knowledge transfer with complete information preservation
- **Scope Isolation**: Sub-agents focus exclusively on assigned domains
- **Parallel Execution**: Independent tasks for maximum efficiency
- **Checkpoint Integration**: Strategic pause points for feedback
- **Complexity Adaptation**: Scales based on project requirements

## Unified Orchestration Prompt

```
I need to [EXECUTE PROJECT TYPE] for [PROJECT DESCRIPTION]. Store findings in [DOCUMENT_DIRECTORY]. Follow this file-based strategic orchestration framework:

**PROJECT TYPES:**
- **MARKET RESEARCH**: "conduct market demand analysis"
- **IDEA MANIFESTATION**: "manifest idea from concept to reality" 
- **STRATEGIC PLANNING**: "create strategic plan"

**PHASE 0 - CONTEXT PREPARATION:**
1. Create directory structure based on project type:
   - Market Research: /foundation/, /competition/, /demand/, /validation/, /opportunity/, /strategy/
   - Idea Manifestation: /ideation/, /evaluation/, /planning/, /execution/, /testing/, /launch/
   - Strategic Planning: /analysis/, /architecture/, /planning/, /framework/
2. Analyze project category, scope, complexity, resource implications
3. Create: [DOCUMENT_DIRECTORY]/project_context.md

**MARKET RESEARCH WORKFLOW:**

**Phase 1 - Foundation (5 Parallel Sub-Agents):**
- Market Sizing → /foundation/market_sizing_analysis.md
- Industry Analysis → /foundation/industry_analysis.md  
- Customer Segmentation → /foundation/customer_segmentation_analysis.md
- Trend Analysis → /foundation/trend_analysis.md
- Regulatory Analysis → /foundation/regulatory_analysis.md

**Phase 2 - Competition (4 Parallel Sub-Agents):**
- Direct Competition (reads: market_sizing, industry) → /competition/direct_competition_analysis.md
- Indirect Competition (reads: industry, trend) → /competition/indirect_competition_analysis.md
- Market Positioning (reads: customer_segmentation, trend) → /competition/market_positioning_analysis.md
- Competitive Intelligence (reads: industry) → /competition/competitive_intelligence_analysis.md

**Phase 3 - Demand (6 Parallel Sub-Agents):**
- Customer Needs (reads: customer_segmentation, market_positioning) → /demand/customer_needs_analysis.md
- Purchase Behavior (reads: customer_segmentation) → /demand/purchase_behavior_analysis.md
- Price Sensitivity (reads: market_sizing, direct_competition) → /demand/price_sensitivity_analysis.md
- Channel Preference (reads: customer_segmentation) → /demand/channel_preference_analysis.md
- Geographic Demand (reads: market_sizing, regulatory) → /demand/geographic_demand_analysis.md
- Seasonal Patterns (reads: trend) → /demand/seasonal_patterns_analysis.md

**Phase 4 - Validation (4 Parallel Sub-Agents):**
- Primary Research (reads: customer_needs, purchase_behavior) → /validation/primary_research_analysis.md
- Secondary Data (reads: market_sizing, industry) → /validation/secondary_data_analysis.md
- Digital Evidence (reads: customer_needs, trend) → /validation/digital_evidence_analysis.md
- Pilot Testing (reads: price_sensitivity, channel_preference) → /validation/pilot_testing_analysis.md

**Phase 5 - Opportunity (5 Parallel Sub-Agents):**
- Market Entry (reads: competitive_intelligence, regulatory) → /opportunity/market_entry_analysis.md
- Revenue Potential (reads: market_sizing, price_sensitivity) → /opportunity/revenue_potential_analysis.md
- Risk Assessment (reads: competitive_intelligence, regulatory) → /opportunity/risk_assessment_analysis.md
- Growth Potential (reads: trend, geographic_demand) → /opportunity/growth_potential_analysis.md
- Investment Viability (reads: revenue_potential, market_entry) → /opportunity/investment_viability_analysis.md

**Phase 6 - Strategy (3 Sequential Sub-Agents):**
- Market Strategy (reads: all competition/, all opportunity/) → /strategy/market_strategy_analysis.md
- Business Case (reads: revenue_potential, investment_viability, market_strategy) → /strategy/business_case_analysis.md
- Research Report (reads: all documents) → /strategy/comprehensive_research_report.md

**IDEA MANIFESTATION WORKFLOW:**
- Phase 1: Ideation (Creative Expansion, Synthesis, Documentation)
- Phase 2: Evaluation (Criteria, Feasibility, Market Assessment, Selection)
- Phase 3: Planning (Project, Resource, Timeline, Risk, Success Metrics)
- Phase 4: Execution (Coordination, Progress Tracking, Adaptation)
- Phase 5: Testing (Prototype, Feedback, Analysis, QA)
- Phase 6: Launch (Preparation, Execution, Post-Launch Evaluation)

**STRATEGIC PLANNING WORKFLOW:**
- Phase 1A: Foundation Analysis (Context, Requirements, Feasibility, Risk)
- Phase 1B: Decomposition (Goal Breakdown, Resource Analysis, Dependencies)
- Phase 2: Solution Architecture (Architecture Design, Implementation Strategy)
- Phase 3: Detailed Planning (Timeline, Resources, Risk Management, QA, Communication)
- Phase 4: Execution Framework (Governance, Monitoring, Adaptation)

**Document Template:**
```markdown
# [Domain] Analysis
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Project Context:** [Brief description]

## Executive Summary
[Brief overview]

## Detailed Analysis
[Comprehensive analysis]

## Key Findings
[Critical insights]

## Data Sources and Methodology
[Sources and approach]

## Integration Points
[Cross-domain relationships]

## Confidence Assessment
[Data quality evaluation]
```

**Conflict Resolution:**
1. Main Agent identifies document contradictions
2. Create conflict_resolution_[timestamp].md
3. Re-run affected sub-agents with conflict context
4. Continue with updated documents

**Complexity Adaptation:**
- Simple (< 1 month): Abbreviated workflow, reduced sub-agents
- Medium (1-6 months): Full workflow as described
- Complex (6+ months): Extended workflow, additional sub-agents

**Options:** [PROJECT TYPE] for [PROJECT DESCRIPTION] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW FOUNDATION | REVIEW STRATEGY | REVIEW PLANNING]
```

## Key Benefits

### Information Preservation
- **Complete Data Retention**: No loss through summarization
- **Detailed Context**: Rich documentation for each domain
- **Historical Record**: Complete audit trail
- **Knowledge Building**: Persistent documentation for future projects

### Enhanced Collaboration  
- **Selective Context**: Sub-agents read only relevant documents
- **Parallel Safety**: Independent work without interference
- **Conflict Detection**: Systematic document comparison
- **Quality Assurance**: Document-based validation

### Strategic Advantages
- **Scalable Communication**: File system handles complex data
- **Audit Compliance**: Complete documentation trail
- **Team Knowledge**: Shared understanding through documentation
- **Continuous Improvement**: Captured patterns for optimization

## Quality Standards
- **Evidence-Based**: Conclusions supported by data
- **Multi-Source Validation**: Key findings validated independently
- **Methodology Transparency**: Clear research methods
- **Actionable Outcomes**: Clear, implementable guidance
