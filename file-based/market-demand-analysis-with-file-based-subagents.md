# How to Conduct Market Demand Analysis Using File-Based Sub-Agent Communication

## Overview
This workflow systematically analyzes market demand through comprehensive research phases and specialized sub-agent delegation with persistent file-based communication. Each research phase creates detailed documentation, ensuring thorough analysis and data-driven insights for commercial viability assessment.

## Complete Market Demand Analysis Workflow Prompt

```
I need to conduct comprehensive market demand analysis for [TOPIC/CONCEPT/IDEA DESCRIPTION]. Store all sub-agent research in [DOCUMENT_DIRECTORY]. Follow this file-based market research workflow:

**PHASE 0 - RESEARCH SCOPE & CONTEXT PREPARATION (Main Agent):**
1. Create document directory structure in [DOCUMENT_DIRECTORY]:
   - /phase_1_foundation/
   - /phase_2_competition/
   - /phase_3_demand/
   - /phase_4_validation/
   - /phase_5_opportunity/
   - /phase_6_strategy/
2. Check existing knowledge graph for related market research, industry patterns, and analysis methodologies
3. Analyze the topic/concept to determine:
   - **Research Category**: Product/service, content/media, business model, technology solution, market trend, consumer behavior
   - **Market Scope**: Local, regional, national, international, niche, mass market
   - **Industry Context**: Established market, emerging sector, disruptive innovation, traditional industry
   - **Analysis Depth**: Surface validation, comprehensive analysis, strategic planning, investment decision support
4. Define research objectives and key questions to be answered
5. Create initial todo breakdown using todo_write with research phases
6. Create: [DOCUMENT_DIRECTORY]/research_scope.md (documenting research objectives and methodology)
7. **CHECKPOINT 0**: If checkpoints enabled, confirm research scope and methodology approach

**PHASE 1 - FOUNDATIONAL MARKET RESEARCH (5 Parallel Sub-Agents):**
8. Deploy FIVE parallel sub-agents simultaneously for comprehensive market foundation:

   **Market Sizing Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/research_scope.md
   - Perform: Market sizing analysis - research total addressable market (TAM), serviceable addressable market (SAM), serviceable obtainable market (SOM), quantitative data gathering, growth projections
   - Create: [DOCUMENT_DIRECTORY]/phase_1_foundation/market_sizing_analysis.md (documenting completed market sizing research)

   **Industry Analysis Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/research_scope.md
   - Perform: Industry structure analysis - analyze industry players, market maturity, regulatory environment, industry-specific factors affecting demand
   - Create: [DOCUMENT_DIRECTORY]/phase_1_foundation/industry_analysis.md (documenting completed industry research)

   **Customer Segmentation Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/research_scope.md
   - Perform: Customer segmentation analysis - identify target customer segments, demographics, psychographics, behavior patterns, purchasing decision factors
   - Create: [DOCUMENT_DIRECTORY]/phase_1_foundation/customer_segmentation_analysis.md (documenting completed segmentation research)

   **Trend Analysis Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/research_scope.md
   - Perform: Market trend analysis - research market trends, emerging patterns, technology adoption curves, future market direction indicators
   - Create: [DOCUMENT_DIRECTORY]/phase_1_foundation/trend_analysis.md (documenting completed trend research)

   **Regulatory Analysis Sub-Agent:**
   - Read: [DOCUMENT_DIRECTORY]/research_scope.md
   - Perform: Regulatory environment analysis - analyze relevant regulations, compliance requirements, policy impacts, legal considerations affecting market demand
   - Create: [DOCUMENT_DIRECTORY]/phase_1_foundation/regulatory_analysis.md (documenting completed regulatory research)

9. Main Agent: Read all foundational research documents, synthesize findings, resolve data conflicts
10. **IF CONTRADICTIONS FOUND**: Repeat relevant Phase 1 sub-agents with clarified scope and conflict resolution instructions
11. **CHECKPOINT 1**: If checkpoints enabled, review foundational market research and validate key findings

**PHASE 2 - COMPETITIVE LANDSCAPE & POSITIONING ANALYSIS (4 Parallel Sub-Agents):**
12. Deploy FOUR parallel sub-agents simultaneously:

    **Direct Competition Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/market_sizing_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/industry_analysis.md
    - Perform: Direct competition analysis - identify direct competitors, analyze offerings, market share, pricing strategies, competitive advantages
    - Create: [DOCUMENT_DIRECTORY]/phase_2_competition/direct_competition_analysis.md (documenting completed direct competition research)

    **Indirect Competition Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/market_sizing_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/industry_analysis.md
    - Perform: Indirect competition analysis - research alternative solutions, substitute products/services, broader competitive threats
    - Create: [DOCUMENT_DIRECTORY]/phase_2_competition/indirect_competition_analysis.md (documenting completed indirect competition research)

    **Market Positioning Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/customer_segmentation_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/trend_analysis.md
    - Perform: Market positioning analysis - analyze competitive positioning, market gaps, differentiation opportunities, unique value propositions
    - Create: [DOCUMENT_DIRECTORY]/phase_2_competition/market_positioning_analysis.md (documenting completed positioning research)

    **Competitive Intelligence Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/industry_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/trend_analysis.md
    - Perform: Competitive intelligence gathering - collect intelligence on competitor strategies, recent moves, financial performance, market positioning
    - Create: [DOCUMENT_DIRECTORY]/phase_2_competition/competitive_intelligence_analysis.md (documenting completed intelligence research)

13. Main Agent: Read all competitive analysis documents, synthesize findings, identify market opportunities
14. **IF COMPETITIVE CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
15. **CHECKPOINT 2**: If checkpoints enabled, review competitive landscape and positioning opportunities

**PHASE 3 - CUSTOMER DEMAND & BEHAVIOR ANALYSIS (6 Parallel Sub-Agents):**
16. Deploy SIX parallel sub-agents for comprehensive demand analysis:

    **Customer Needs Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/customer_segmentation_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_competition/market_positioning_analysis.md
    - Perform: Customer needs analysis - research customer pain points, unmet needs, job-to-be-done analysis, demand drivers
    - Create: [DOCUMENT_DIRECTORY]/phase_3_demand/customer_needs_analysis.md (documenting completed needs research)

    **Purchase Behavior Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/customer_segmentation_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_competition/direct_competition_analysis.md
    - Perform: Purchase behavior analysis - analyze customer purchase patterns, decision-making processes, buying criteria, conversion factors
    - Create: [DOCUMENT_DIRECTORY]/phase_3_demand/purchase_behavior_analysis.md (documenting completed behavior research)

    **Price Sensitivity Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/market_sizing_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_2_competition/direct_competition_analysis.md
    - Perform: Price sensitivity analysis - research pricing expectations, willingness to pay, price elasticity, monetization potential
    - Create: [DOCUMENT_DIRECTORY]/phase_3_demand/price_sensitivity_analysis.md (documenting completed pricing research)

    **Channel Preference Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/customer_segmentation_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/trend_analysis.md
    - Perform: Channel preference analysis - analyze preferred distribution channels, sales mechanisms, customer acquisition pathways
    - Create: [DOCUMENT_DIRECTORY]/phase_3_demand/channel_preference_analysis.md (documenting completed channel research)

    **Geographic Demand Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/market_sizing_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/regulatory_analysis.md
    - Perform: Geographic demand analysis - research geographic demand variations, regional preferences, market penetration opportunities
    - Create: [DOCUMENT_DIRECTORY]/phase_3_demand/geographic_demand_analysis.md (documenting completed geographic research)

    **Seasonal Patterns Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/trend_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_demand/customer_needs_analysis.md (wait for completion)
    - Perform: Seasonal patterns analysis - analyze demand seasonality, cyclical patterns, timing considerations for market entry
    - Create: [DOCUMENT_DIRECTORY]/phase_3_demand/seasonal_patterns_analysis.md (documenting completed seasonal research)

17. Main Agent: Read all customer demand documents, integrate insights
18. **IF DEMAND CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
19. **CHECKPOINT 3**: If checkpoints enabled, review customer demand analysis and behavior patterns

**PHASE 4 - MARKET VALIDATION & EVIDENCE GATHERING (4 Parallel Sub-Agents):**
20. Deploy FOUR parallel sub-agents for validation research:

    **Primary Research Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_demand/customer_needs_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_demand/purchase_behavior_analysis.md
    - Perform: Primary research execution - design and conduct surveys, interviews, focus groups, direct customer research to validate demand assumptions
    - Create: [DOCUMENT_DIRECTORY]/phase_4_validation/primary_research_analysis.md (documenting completed primary research)

    **Secondary Data Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/market_sizing_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/industry_analysis.md
    - Perform: Secondary data gathering - collect market reports, industry studies, academic research, third-party validation data
    - Create: [DOCUMENT_DIRECTORY]/phase_4_validation/secondary_data_analysis.md (documenting completed secondary research)

    **Digital Evidence Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_demand/customer_needs_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/trend_analysis.md
    - Perform: Digital evidence analysis - analyze search volume data, social media trends, online discussions, digital demand signals
    - Create: [DOCUMENT_DIRECTORY]/phase_4_validation/digital_evidence_analysis.md (documenting completed digital research)

    **Pilot Testing Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_3_demand/price_sensitivity_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_demand/channel_preference_analysis.md
    - Perform: Pilot testing design - design market testing approaches, MVP validation strategies, demand proof concepts
    - Create: [DOCUMENT_DIRECTORY]/phase_4_validation/pilot_testing_analysis.md (documenting completed testing design)

21. Main Agent: Read all validation documents, validate research findings, resolve conflicting evidence
22. **IF VALIDATION CONFLICTS**: Create conflict resolution document and re-run affected sub-agents
23. **CHECKPOINT 4**: If checkpoints enabled, review validation evidence and research reliability

**PHASE 5 - MARKET OPPORTUNITY & RISK ASSESSMENT (5 Parallel Sub-Agents):**
24. Deploy FIVE parallel sub-agents for comprehensive opportunity evaluation:

    **Market Entry Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_competition/competitive_intelligence_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/regulatory_analysis.md
    - Perform: Market entry analysis - assess barriers to entry, startup costs, required capabilities, market entry strategies
    - Create: [DOCUMENT_DIRECTORY]/phase_5_opportunity/market_entry_analysis.md (documenting completed entry analysis)

    **Revenue Potential Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/market_sizing_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_demand/price_sensitivity_analysis.md
    - Perform: Revenue potential analysis - calculate revenue projections, monetization models, pricing strategies, financial opportunity assessment
    - Create: [DOCUMENT_DIRECTORY]/phase_5_opportunity/revenue_potential_analysis.md (documenting completed revenue analysis)

    **Risk Assessment Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_2_competition/competitive_intelligence_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/regulatory_analysis.md
    - Perform: Risk assessment analysis - identify market risks, competitive threats, economic factors, potential failure scenarios
    - Create: [DOCUMENT_DIRECTORY]/phase_5_opportunity/risk_assessment_analysis.md (documenting completed risk analysis)

    **Growth Potential Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_1_foundation/trend_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_3_demand/geographic_demand_analysis.md
    - Perform: Growth potential analysis - analyze scalability opportunities, expansion potential, long-term growth trajectories
    - Create: [DOCUMENT_DIRECTORY]/phase_5_opportunity/growth_potential_analysis.md (documenting completed growth analysis)

    **Investment Viability Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_5_opportunity/revenue_potential_analysis.md (wait for completion)
    - Read: [DOCUMENT_DIRECTORY]/phase_5_opportunity/market_entry_analysis.md (wait for completion)
    - Perform: Investment viability analysis - assess investment requirements, ROI potential, payback periods, financial attractiveness
    - Create: [DOCUMENT_DIRECTORY]/phase_5_opportunity/investment_viability_analysis.md (documenting completed investment analysis)

25. Main Agent: Read all opportunity assessment documents, synthesize evaluation
26. **IF OPPORTUNITY CONFLICTS**: Create conflict resolution document and re-run conflicting sub-agents
27. **CHECKPOINT 5**: If checkpoints enabled, review opportunity evaluation and risk analysis

**PHASE 6 - STRATEGIC RECOMMENDATIONS & REPORTING (3 Sequential Sub-Agents):**
28. Deploy THREE sub-agents sequentially for final analysis and recommendations:

    **Market Strategy Sub-Agent:**
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_2_competition/
    - Read: All documents from [DOCUMENT_DIRECTORY]/phase_5_opportunity/
    - Perform: Market strategy development - develop market entry strategy, positioning recommendations, tactical approaches
    - Create: [DOCUMENT_DIRECTORY]/phase_6_strategy/market_strategy_analysis.md (documenting completed strategy development)

    **Business Case Sub-Agent:**
    - Read: [DOCUMENT_DIRECTORY]/phase_5_opportunity/revenue_potential_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_5_opportunity/investment_viability_analysis.md
    - Read: [DOCUMENT_DIRECTORY]/phase_6_strategy/market_strategy_analysis.md
    - Perform: Business case development - create business case analysis, financial projections, investment recommendations
    - Create: [DOCUMENT_DIRECTORY]/phase_6_strategy/business_case_analysis.md (documenting completed business case)

    **Research Report Sub-Agent:**
    - Read: All documents from all phases
    - Perform: Comprehensive report compilation - compile comprehensive market research report with executive summary, findings, actionable insights
    - Create: [DOCUMENT_DIRECTORY]/phase_6_strategy/comprehensive_research_report.md (documenting completed research report)

29. Main Agent: Review final outputs, update knowledge graph with market research patterns, deliver comprehensive analysis

**DOCUMENT STRUCTURE REQUIREMENTS:**

Each sub-agent document must include:

"""markdown
# [Domain] Market Analysis
**Agent:** [Sub-Agent Name]
**Phase:** [Phase Number]
**Timestamp:** [ISO Timestamp]
**Documents Read:** [List of input documents]
**Research Focus:** [Specific research domain]

## Executive Summary
[Brief overview of research completed]

## Detailed Research Findings
[Comprehensive analysis within research domain]

## Data Sources and Methodology
[Sources used and research approach]

## Key Insights and Implications
[Critical insights for market understanding]

## Integration Points
[How findings relate to other research domains]

## Confidence Assessment
[Data quality and reliability assessment]
"""

**MARKET RESEARCH SCOPE ISOLATION:**
- **Foundation sub-agents focus only on their research domain** without analyzing opportunities
- **Competition sub-agents analyze competitive landscape only** without making strategic recommendations
- **Demand sub-agents research customer behavior patterns** without evaluating business viability
- **Validation sub-agents gather evidence systematically** without drawing strategic conclusions
- **Opportunity sub-agents assess potential only** without implementing strategies
- **Strategy sub-agents synthesize insights into recommendations** after all research phases complete

**CONFLICT RESOLUTION PROTOCOL:**
1. Main Agent identifies contradictions between research documents
2. Create conflict_resolution_[timestamp].md documenting specific conflicts
3. Re-run affected sub-agents with conflict context and additional guidance
4. Continue workflow with updated documents

**RESEARCH COMPLEXITY ADAPTATION:**
- **Simple Validation (< 1 week)**: Use abbreviated workflow focusing on Phases 1, 3, and 6 with reduced sub-agent deployment
- **Standard Analysis (1-4 weeks)**: Use full workflow with standard sub-agent delegation as described
- **Comprehensive Study (4+ weeks)**: Use extended workflow with additional sub-agents for specialized industry research

**HUMAN FEEDBACK OPTIONS:**
- **Default**: Fully autonomous execution with comprehensive market research report
- **Add "WITH CHECKPOINTS"**: Pause after each major phase for review and research direction guidance
- **Add "REVIEW FOUNDATION"**: Pause only after Phase 1 to confirm foundational research
- **Add "REVIEW COMPETITION"**: Pause only after Phase 2 to validate competitive insights
- **Add "REVIEW VALIDATION"**: Pause only after Phase 4 to confirm evidence quality

**TOPIC/CONCEPT/IDEA TO RESEARCH:**
[TOPIC/CONCEPT/IDEA DESCRIPTION] using document directory [DOCUMENT_DIRECTORY] [OPTIONAL: WITH CHECKPOINTS | REVIEW FOUNDATION | REVIEW COMPETITION | REVIEW VALIDATION]

Begin with Phase 0 research scope preparation and proceed systematically through each market analysis phase with validation checkpoints.
```

## Usage Instructions

1. **Replace placeholders** with specific information:
   - `[TOPIC/CONCEPT/IDEA DESCRIPTION]` - Detailed description including target market, geographic scope, industry context, research purpose
   - `[DOCUMENT_DIRECTORY]` - Absolute path where documents should be stored (e.g., "/project/research/ai-productivity-tools")

2. **Prepare document directory** - Ensure the specified directory exists and is writable

3. **Choose feedback level** by adding optional modifiers for human checkpoints

4. **Research complexity determines workflow depth** - Simple validation uses abbreviated workflow, comprehensive studies use extended workflow

## Key Benefits of File-Based Communication

- **Comprehensive Research Documentation**: Complete preservation of all research findings and methodologies
- **Multi-Source Validation**: Systematic cross-referencing of research findings across documents
- **Research Continuity**: Persistent knowledge base for future market research and updates
- **Quality Assurance**: Systematic validation through document comparison and conflict resolution
- **Strategic Synthesis**: Clear progression from foundational research to actionable strategy
- **Audit Trail**: Complete record of research methodology, sources, and decision-making process

## Document Organization Example

```
/project/research/ai-productivity-tools/
├── research_scope.md
├── phase_1_foundation/
│   ├── market_sizing_analysis.md
│   ├── industry_analysis.md
│   ├── customer_segmentation_analysis.md
│   ├── trend_analysis.md
│   └── regulatory_analysis.md
├── phase_2_competition/
│   ├── direct_competition_analysis.md
│   ├── indirect_competition_analysis.md
│   ├── market_positioning_analysis.md
│   └── competitive_intelligence_analysis.md
├── phase_3_demand/
│   ├── customer_needs_analysis.md
│   ├── purchase_behavior_analysis.md
│   ├── price_sensitivity_analysis.md
│   ├── channel_preference_analysis.md
│   ├── geographic_demand_analysis.md
│   └── seasonal_patterns_analysis.md
├── phase_4_validation/
│   ├── primary_research_analysis.md
│   ├── secondary_data_analysis.md
│   ├── digital_evidence_analysis.md
│   └── pilot_testing_analysis.md
├── phase_5_opportunity/
│   ├── market_entry_analysis.md
│   ├── revenue_potential_analysis.md
│   ├── risk_assessment_analysis.md
│   ├── growth_potential_analysis.md
│   └── investment_viability_analysis.md
└── phase_6_strategy/
    ├── market_strategy_analysis.md
    ├── business_case_analysis.md
    └── comprehensive_research_report.md
```

## Research Quality Standards

- **Data-Driven Analysis**: All conclusions supported by quantitative data and qualitative evidence
- **Multi-Source Validation**: Key findings validated through multiple independent research sources
- **Methodology Transparency**: Research methods, sources, and analytical approaches documented
- **Bias Recognition**: Research limitations, potential biases, and confidence levels acknowledged
- **Actionable Insights**: Research outputs provide clear, implementable recommendations

## Advanced Features

- **Knowledge Building**: Market research patterns and methodologies captured for future use
- **Cross-Project Learning**: Research findings inform related market analysis projects
- **Incremental Updates**: Ability to update specific research domains without complete re-analysis
- **Competitive Monitoring**: Framework for ongoing competitive intelligence gathering
- **Market Tracking**: Systematic approach for monitoring market changes over time
