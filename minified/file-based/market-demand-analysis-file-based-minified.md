# Market Demand Analysis with File-Based Sub-Agents (Minified)

## Workflow Prompt

```
I need to conduct market demand analysis for [TOPIC/CONCEPT/IDEA]. Store research in [DOCUMENT_DIRECTORY]. Follow this file-based market research workflow:

**PHASE 0 - RESEARCH SCOPE:**
1. Create directories: /foundation/, /competition/, /demand/, /validation/, /opportunity/, /strategy/
2. Analyze research category, scope, industry context, analysis depth
3. Create: [DOCUMENT_DIRECTORY]/research_scope.md

**PHASE 1 - FOUNDATIONAL RESEARCH (5 Parallel Sub-Agents):**

**Market Sizing Sub-Agent:**
- Read: research_scope.md
- Perform: TAM, SAM, SOM research, quantitative data, growth projections
- Create: /foundation/market_sizing_analysis.md

**Industry Analysis Sub-Agent:**
- Read: research_scope.md
- Perform: Industry structure, players, maturity, regulations
- Create: /foundation/industry_analysis.md

**Customer Segmentation Sub-Agent:**
- Read: research_scope.md
- Perform: Target segments, demographics, behavior patterns
- Create: /foundation/customer_segmentation_analysis.md

**Trend Analysis Sub-Agent:**
- Read: research_scope.md
- Perform: Market trends, emerging patterns, adoption curves
- Create: /foundation/trend_analysis.md

**Regulatory Analysis Sub-Agent:**
- Read: research_scope.md
- Perform: Regulations, compliance, policy impacts
- Create: /foundation/regulatory_analysis.md

**PHASE 2 - COMPETITIVE ANALYSIS (4 Parallel Sub-Agents):**

**Direct Competition Sub-Agent:**
- Read: market_sizing_analysis.md, industry_analysis.md
- Perform: Direct competitors, market share, pricing strategies
- Create: /competition/direct_competition_analysis.md

**Indirect Competition Sub-Agent:**
- Read: industry_analysis.md, trend_analysis.md
- Perform: Alternatives, substitutes, broader threats
- Create: /competition/indirect_competition_analysis.md

**Market Positioning Sub-Agent:**
- Read: customer_segmentation_analysis.md, trend_analysis.md
- Perform: Positioning gaps, differentiation opportunities
- Create: /competition/market_positioning_analysis.md

**Competitive Intelligence Sub-Agent:**
- Read: industry_analysis.md, trend_analysis.md
- Perform: Competitor strategies, financial performance
- Create: /competition/competitive_intelligence_analysis.md

**PHASE 3 - DEMAND ANALYSIS (6 Parallel Sub-Agents):**

**Customer Needs Sub-Agent:**
- Read: customer_segmentation_analysis.md, market_positioning_analysis.md
- Perform: Pain points, unmet needs, demand drivers
- Create: /demand/customer_needs_analysis.md

**Purchase Behavior Sub-Agent:**
- Read: customer_segmentation_analysis.md, direct_competition_analysis.md
- Perform: Decision processes, buying criteria, conversion factors
- Create: /demand/purchase_behavior_analysis.md

**Price Sensitivity Sub-Agent:**
- Read: market_sizing_analysis.md, direct_competition_analysis.md
- Perform: Pricing expectations, willingness to pay, elasticity
- Create: /demand/price_sensitivity_analysis.md

**Channel Preference Sub-Agent:**
- Read: customer_segmentation_analysis.md, trend_analysis.md
- Perform: Distribution channels, acquisition pathways
- Create: /demand/channel_preference_analysis.md

**Geographic Demand Sub-Agent:**
- Read: market_sizing_analysis.md, regulatory_analysis.md
- Perform: Regional variations, penetration opportunities
- Create: /demand/geographic_demand_analysis.md

**Seasonal Patterns Sub-Agent:**
- Read: trend_analysis.md, customer_needs_analysis.md
- Perform: Demand seasonality, cyclical patterns
- Create: /demand/seasonal_patterns_analysis.md

**PHASE 4 - VALIDATION (4 Parallel Sub-Agents):**

**Primary Research Sub-Agent:**
- Read: customer_needs_analysis.md, purchase_behavior_analysis.md
- Perform: Surveys, interviews, direct customer research
- Create: /validation/primary_research_analysis.md

**Secondary Data Sub-Agent:**
- Read: market_sizing_analysis.md, industry_analysis.md
- Perform: Market reports, studies, validation data
- Create: /validation/secondary_data_analysis.md

**Digital Evidence Sub-Agent:**
- Read: customer_needs_analysis.md, trend_analysis.md
- Perform: Search volume, social trends, demand signals
- Create: /validation/digital_evidence_analysis.md

**Pilot Testing Sub-Agent:**
- Read: price_sensitivity_analysis.md, channel_preference_analysis.md
- Perform: Testing approaches, MVP validation strategies
- Create: /validation/pilot_testing_analysis.md

**PHASE 5 - OPPORTUNITY ASSESSMENT (5 Parallel Sub-Agents):**

**Market Entry Sub-Agent:**
- Read: competitive_intelligence_analysis.md, regulatory_analysis.md
- Perform: Barriers, costs, required capabilities
- Create: /opportunity/market_entry_analysis.md

**Revenue Potential Sub-Agent:**
- Read: market_sizing_analysis.md, price_sensitivity_analysis.md
- Perform: Revenue projections, monetization models
- Create: /opportunity/revenue_potential_analysis.md

**Risk Assessment Sub-Agent:**
- Read: competitive_intelligence_analysis.md, regulatory_analysis.md
- Perform: Market risks, competitive threats, failure scenarios
- Create: /opportunity/risk_assessment_analysis.md

**Growth Potential Sub-Agent:**
- Read: trend_analysis.md, geographic_demand_analysis.md
- Perform: Scalability, expansion potential, growth trajectories
- Create: /opportunity/growth_potential_analysis.md

**Investment Viability Sub-Agent:**
- Read: revenue_potential_analysis.md, market_entry_analysis.md
- Perform: Investment requirements, ROI, financial attractiveness
- Create: /opportunity/investment_viability_analysis.md

**PHASE 6 - STRATEGY (3 Sequential Sub-Agents):**

**Market Strategy Sub-Agent:**
- Read: All competition/ and opportunity/ documents
- Perform: Market entry strategy, positioning recommendations
- Create: /strategy/market_strategy_analysis.md

**Business Case Sub-Agent:**
- Read: revenue_potential_analysis.md, investment_viability_analysis.md, market_strategy_analysis.md
- Perform: Business case analysis, financial projections
- Create: /strategy/business_case_analysis.md

**Research Report Sub-Agent:**
- Read: All documents from all phases
- Perform: Comprehensive report compilation
- Create: /strategy/comprehensive_research_report.md

**Document Template:**
```markdown
# [Domain] Market Analysis
**Agent:** [Name] | **Phase:** [N] | **Timestamp:** [ISO]
**Documents Read:** [List] | **Research Focus:** [Domain]

## Executive Summary
[Brief overview]

## Detailed Research Findings
[Comprehensive analysis]

## Data Sources and Methodology
[Sources and approach]

## Key Insights and Implications
[Critical insights]

## Integration Points
[Cross-domain relationships]

## Confidence Assessment
[Data quality evaluation]
```

**Options:** [TOPIC/CONCEPT/IDEA] using [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW FOUNDATION | REVIEW COMPETITION | REVIEW VALIDATION]
```

## Key Benefits
- **Complete Research Documentation**: All findings preserved with sources
- **Multi-Source Validation**: Cross-referencing findings across documents
- **Strategic Synthesis**: Clear progression from research to strategy
- **Knowledge Building**: Market research patterns captured for future use
