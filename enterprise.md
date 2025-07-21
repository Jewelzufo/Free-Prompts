# IBM Granite 3.3 Optimized Prompts

### Template 1: Enterprise Customer Behavior Analysis

```text
Analyze customer data for {company_name} using the following approach:

OBJECTIVE: {analysis_goal}
DATA SOURCE: {data_location}
TIMEFRAME: {analysis_period}

REQUIRED OUTPUTS:
1. Key behavioral patterns (3-5 insights)
2. Actionable recommendations (3 specific items)
3. Business impact assessment (quantified)

ANALYSIS STEPS:
Step 1: Data validation and cleaning
Step 2: Pattern identification using {analysis_method}
Step 3: Business context integration
Step 4: Recommendation formulation

FORMAT: Executive summary + detailed findings
```

### Template 2: Financial Performance Analysis

```text
Conduct financial analysis for {business_unit} with these parameters:

INPUT DATA: {financial_data_source}
METRICS: {key_metrics_list}
BENCHMARK: {comparison_baseline}

DELIVER:
- Performance vs. target (percentage variance)
- Trend analysis (3-month minimum)
- Risk factors identification
- Strategic recommendations

CONSTRAINTS:
- Use GAAP standards
- Include confidence intervals
- Highlight material changes >5%
```

---

## 2. Revised Basic Templates 

### Enhanced Zero-Shot Business Prompting

```text
CONTEXT: {business_domain}
TASK: {specific_business_task}
AUDIENCE: {target_stakeholder_level}

REQUIREMENTS:
- Include industry best practices
- Provide actionable insights
- Consider regulatory compliance
- Format for business presentation

DELIVERABLE: {output_format}
SUCCESS CRITERIA: {measurable_outcomes}
```

### Enhanced Few-Shot Enterprise Prompting

```text
PATTERN RECOGNITION TASK:

EXAMPLE 1: {business_scenario_1} → {solution_approach_1}
EXAMPLE 2: {business_scenario_2} → {solution_approach_2}
EXAMPLE 3: {business_scenario_3} → {solution_approach_3}

NEW SCENARIO: {target_scenario}
APPLY PATTERN: Use established approach for {target_scenario}

ENTERPRISE CONSIDERATIONS:
- ROI implications
- Resource requirements
- Implementation timeline
- Risk mitigation
```

---

## 3. Revised Novel Templates 

### Enterprise Constraint-Driven Problem Solver

```text
BUSINESS CHALLENGE: {problem_statement}
OPERATING CONSTRAINTS:
- Budget: {budget_limit}
- Timeline: {deadline}
- Resources: {available_resources}
- Compliance: {regulatory_requirements}

INNOVATION FRAMEWORK:
1. Constraint analysis
2. Solution ideation within bounds
3. Feasibility assessment
4. Implementation roadmap

OUTPUT: 3-5 ranked solutions with business justification
```

### Strategic Role-Swapping Analysis

```text
SCENARIO: {business_situation}

PERSPECTIVES TO ANALYZE:
Role A: {stakeholder_1} (priorities: {priorities_1})
Role B: {stakeholder_2} (priorities: {priorities_2})
Role C: {stakeholder_3} (priorities: {priorities_3})

FOR EACH PERSPECTIVE:
- Key concerns and opportunities
- Success metrics
- Resource requirements
- Implementation preferences

SYNTHESIS: Identify convergent strategy addressing all stakeholder needs
```

---

## 4. Enhanced AI Engineering Templates 

### Enterprise ML Pipeline Design

```text
BUSINESS PROBLEM: {problem_definition}
SUCCESS METRICS: {kpi_targets}

TECHNICAL REQUIREMENTS:
- Data sources: {data_inventory}
- Model performance: {accuracy_threshold}
- Latency requirements: {response_time_sla}
- Scalability needs: {volume_projections}

DELIVERABLES:
1. Architecture diagram
2. Resource estimation
3. Risk assessment
4. Deployment strategy
5. Monitoring framework

ENTERPRISE CONSIDERATIONS:
- Compliance requirements
- Data governance
- Cost optimization
- Change management
```

### Production-Ready Code Generation

```text
DEVELOPMENT TASK: {coding_objective}
TECHNICAL STACK: {technology_requirements}
ENTERPRISE STANDARDS:
- Security protocols: {security_requirements}
- Testing coverage: {test_requirements}
- Documentation level: {doc_standards}
- Performance criteria: {performance_targets}

CODE DELIVERABLE:
- Main implementation
- Unit tests (>80% coverage)
- Integration tests
- Performance benchmarks
- Security scan results
- Deployment documentation

QUALITY GATES:
- Code review checklist
- Security validation
- Performance validation
```

---

## 5. Advanced Reasoning Templates 

### Enterprise Decision Framework

```text
DECISION CONTEXT: {business_decision}
STAKEHOLDERS: {affected_parties}
TIMELINE: {decision_deadline}

STRUCTURED ANALYSIS:
Step 1: Problem decomposition
- Core issue identification
- Constraint mapping
- Success criteria definition

Step 2: Options evaluation
- Alternative generation (minimum 3)
- Pros/cons analysis
- Risk assessment matrix

Step 3: Impact analysis
- Financial implications
- Operational effects
- Strategic alignment

Step 4: Recommendation synthesis
- Preferred option with rationale
- Implementation plan
- Contingency measures

OUTPUT FORMAT: Executive brief + detailed analysis
```

### Multi-Stakeholder Problem Solving

```text
COMPLEX PROBLEM: {problem_statement}
STAKEHOLDER MAP: {stakeholder_list}

ANALYSIS FRAMEWORK:
Phase 1: Stakeholder perspective mapping
- Each stakeholder's primary concerns
- Success criteria for each group
- Resource constraints per stakeholder

Phase 2: Conflict identification
- Competing interests analysis
- Trade-off implications
- Negotiation opportunities

Phase 3: Solution synthesis
- Win-win opportunity identification
- Compromise scenario development
- Implementation strategy

DELIVERABLE: Stakeholder-aligned solution with implementation roadmap
```

---

## Granite 3.3 Optimization Features

### 1. Token Efficiency Patterns

- Concise instruction formatting
- Structured output requirements
- Clear success criteria
- Minimal repetition

### 2. Enterprise Context Integration

- Business-relevant examples
- ROI considerations
- Compliance awareness
- Stakeholder alignment

### 3. Standardized Placeholder Format

- Consistent `{parameter_name}` syntax
- Clear parameter descriptions
- Logical parameter grouping
- Easy customization

### 4. Enhanced Instruction Clarity

- Step-by-step processes
- Explicit output formats
- Measurable success criteria
- Clear constraint definitions

---

## Implementation Guidelines for Granite 3.3

### Best Practices:

1. **Prefix Context**: Always provide business domain context  
2. **Structure Instructions**: Use numbered steps and clear sections  
3. **Define Success**: Include measurable outcomes  
4. **Consider Constraints**: Explicitly state limitations  
5. **Format Output**: Specify exact deliverable format  

### Avoiding Common Issues:

- Don't use overly verbose instructions
- Avoid ambiguous placeholder names
- Don't mix instruction styles within templates
- Avoid unclear success criteria

### Testing Recommendations:

1. Test with representative enterprise scenarios
2. Validate output quality against business standards
3. Measure response consistency across similar prompts
4. Ensure scalability for production use

---


