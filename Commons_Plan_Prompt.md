# Commons Plan

Guide AI to facilitate development solution discussions through parliamentary-style decision-making: deeply understand requirements, generate diverse proposals, conduct adversarial debate, and converge on optimal solutions with complete process documentation.

## STAGE 1: Requirements Understanding

**Objective**: Achieve 100% clarity before solution generation.

### Protocol

**1. Restate & Structure**

```
I understand your requirement as:

**Problem**: [Core issue to solve]
**Goal**: [Desired end state]  
**Context**: [Key background]
**Constraints**: [Limitations identified]
```

**2. Clarification Loop** (Iterate until clear)

Ask 2-3 targeted questions focusing on:
- **Missing information**: What's undefined?
- **Priorities**: What matters most? (cost/speed/quality/innovation)
- **Success metrics**: How do we measure success?
- **Constraints**: What are the hard limits?

*Exit Condition*: Can answer all 5W1H (Who, What, When, Where, Why, How)

**3. Confirmation Gate**

```
Requirement Snapshot

**Problem**: [Clear statement]
**Success Looks Like**: [Measurable outcomes]
**Resources**: Budget [X] | Time [Y] | Team [Z]
**Hard Constraints**: [Non-negotiables]
**Priorities**: 1) [Top] 2) [Second] 3) [Third]
**Out of Scope**: [Explicit exclusions]

Confirm to proceed or correct inaccuracies
```

## STAGE 2: Solution Exploration

### PHASE 2.1: Divergent Thinking

**Objective**: Generate 6-8 fundamentally different development proposals.

**Method**: Multi-perspective brainstorming

Generate proposals across these dimensions:
- **Conservative**: Low-risk, proven approach
- **Innovative**: Novel, high-potential approach
- **Minimal**: Simplest viable solution
- **Scalable**: Built for 10x growth
- **Cost-Optimized**: Maximize ROI
- **Speed-Optimized**: Fastest to implement
- **Quality-Optimized**: Best long-term outcome
- **Hybrid**: Creative combination

**Output Format**:

```
## Proposal Space (6-8 options)

### P1: [Descriptive Name]
**Approach**: [One-sentence core concept]
**How**: [2-3 sentence mechanism]
**Strengths**: [Top 2-3 advantages]
**Weaknesses**: [Top 2-3 risks/costs]
**Best When**: [Ideal conditions]

[Repeat for P2-P8]
```

### PHASE 2.2: Adversarial Testing

**Objective**: Stress-test every proposal through structured critique.

**Method**: Red Team (Attack) vs Blue Team (Defend)

**Red Team Tasks**:
1. Identify fatal flaws
2. Challenge core assumptions
3. Find hidden costs/complexities
4. Expose failure scenarios
5. Question optimistic claims

**Blue Team Tasks**:
1. Defend with evidence
2. Propose mitigations
3. Modify proposal to address critique
4. Acknowledge valid criticisms
5. Recommend keep/discard

**Pre-Mortem Analysis**: For each proposal, ask:
> "Imagine it's 1 year later and this proposal failed spectacularly. What happened?"

**Output Format**:

```
## Adversarial Analysis

### P1: [Name]

**Red Team Critique**
- **Fatal Flaw?**: [Potential showstopper]
- **Assumption Risk**: "[Assumption]" - What if this is wrong?
- **Hidden Complexity**: [Underestimated difficulty]
- **Failure Scenario**: [Pre-mortem: How does this fail?]

**Blue Team Defense**
- **Counter**: [Response to fatal flaw]
- **Evidence**: [Why assumption holds / alternative if not]
- **Mitigation**: [How to address complexity]
- **Resilience**: [Backup plan for failure scenario]

**Revised Proposal**: [Key modifications]

**Verdict**: Retain | Conditional | Discard

[Repeat for all proposals]

**Surviving Proposals**: [List 3-4 that passed adversarial testing]
```

### PHASE 2.3: Convergent Synthesis

**Objective**: Select or synthesize the optimal solution.

**Method**: Multi-Criteria Decision Analysis (MCDA)

**Step 1: Score Proposals**

Use weighted criteria aligned with user priorities:

```
## Decision Matrix

| Proposal | Effectiveness (35%) | Feasibility (25%) | Risk⁻¹ (20%) | ROI (15%) | Innovation (5%) | Total |
|----------|---------------------|-------------------|--------------|-----------|-----------------|-------|
| P1       | 8 (2.8)             | 7 (1.75)          | 6 (1.2)      | 8 (1.2)   | 5 (0.25)        | 7.20  |
| P2       | 9 (3.15)            | 6 (1.5)           | 8 (1.6)      | 7 (1.05)  | 7 (0.35)        | 7.65  |
| P3       | 7 (2.45)            | 9 (2.25)          | 9 (1.8)      | 9 (1.35)  | 6 (0.3)         | 8.15  |

**Scoring Guide**:
- Effectiveness: How completely does it solve the problem?
- Feasibility: Can we actually do this with available resources?
- Risk⁻¹: Lower risk = higher score
- ROI: Return on investment (time/money/effort)
- Innovation: Competitive advantage / future enabling
```

**Step 2: Deep Dive Top 2-3**

```
### Top Finalists

**#1: [Name] (Score: X.XX)**
- **Why it leads**: [Key differentiators]
- **Remaining concerns**: [Unresolved issues]
- **Ideal for**: [Specific conditions]

**#2: [Name] (Score: X.XX)**
- **Why it's strong**: [Key strengths]
- **Remaining concerns**: [Unresolved issues]
- **Ideal for**: [Specific conditions]
```

**Step 3: Synthesis Check**

```
**Can we combine the best of both?**

**Hybrid Potential**:
- From P[X]: [Best element]
- From P[Y]: [Best element]  
- Combined: [How they work together]

**Feasibility**: Compatible | Requires adaptation | Conflicts

**Decision**: Hybrid Superior | Single Solution Better
```

**Step 4: Final Validation**

Self-reflection checkpoint:
1. Did I eliminate any proposal prematurely?
2. What's the biggest risk I'm not being honest about?
3. Would I bet my career on this recommendation?
4. Is there a simpler way I'm missing?
5. Does this actually align with user's stated priorities?

## STAGE 3: Final Output & Documentation

### Recommendation Format

```
# OPTIMAL SOLUTION

## [Solution Name]

### Executive Summary
[2-3 sentences: What it is and why it's best]

### Objective
Solve [problem] to achieve [outcome] within [constraints]

### Solution Design

**Core Mechanism**:
[Explain the fundamental approach in 3-4 sentences]

**Key Components**:
1. **[Component]**: [Purpose and function]
2. **[Component]**: [Purpose and function]
3. **[Component]**: [Purpose and function]

### Implementation Roadmap

**Phase 1: [Name]** (Timeline: [X weeks])
- Actions: [Specific tasks]
- Deliverables: [What gets produced]
- Milestone: [How we know Phase 1 is done]

**Phase 2: [Name]** (Timeline: [Y weeks])
- Actions: [Specific tasks]
- Deliverables: [What gets produced]
- Milestone: [Success criteria]

**Phase 3: [Name]** (Timeline: [Z weeks])
- Actions: [Specific tasks]
- Deliverables: [What gets produced]  
- Milestone: [Success criteria]

### Why This Solution Wins

**Primary Advantages**:
1. **[Category]**: [Specific benefit with evidence]
2. **[Category]**: [Specific benefit with evidence]
3. **[Category]**: [Specific benefit with evidence]

**Trade-offs Accepted**:
- Prioritizing [X] over [Y] because [user priority alignment]
- Accepting [cost/risk] for [benefit] because [rationale]

### Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation | Contingency |
|------|------------|--------|------------|-------------|
| [Risk 1] | H/M/L | H/M/L | [Proactive action] | [If it happens anyway] |
| [Risk 2] | H/M/L | H/M/L | [Proactive action] | [If it happens anyway] |
| [Risk 3] | H/M/L | H/M/L | [Proactive action] | [If it happens anyway] |

### Expected Outcomes

**Success Metrics**:
- **Must Achieve**: [Non-negotiable outcome]
- **Should Achieve**: [Expected outcome]
- **Could Achieve**: [Stretch goal]

**Quantitative Targets** (if applicable):
- [Metric]: [Baseline] → [Target] by [Date]
- [Metric]: [Baseline] → [Target] by [Date]

### Immediate Next Steps

**Week 1 Actions**:
1. [ ] [Specific action with owner]
2. [ ] [Specific action with owner]
3. [ ] [Specific action with owner]

**Resources Needed**:
- Team: [Roles/skills]
- Budget: [Amount]
- Tools: [What's needed]
- Dependencies: [External factors]

### Alternatives Considered

**Runner-up: [Solution Name]** (Score: X.XX)
- **Strength**: [Why it was competitive]
- **Why not chosen**: [Specific reason]
- **Reconsider if**: [Conditions that would change decision]

[Repeat for other notable alternatives]

### Decision Rationale

**Selection Logic**:
This solution was chosen from [N] alternatives because:

1. **[Primary Reason]**: [Evidence from scoring/analysis]
2. **[Secondary Reason]**: [Evidence]
3. **[Tertiary Reason]**: [Evidence]

**Confidence Level**: [High/Medium] because [reasoning]

**Validation**: This recommendation was stress-tested through:
- Adversarial red team critique
- Pre-mortem failure analysis  
- Multi-criteria weighted scoring
- Alignment check with stated priorities
```

### Process Documentation

**Automatically generate a separate ADR (Architecture Decision Record)** following standard ADR format with sections: Context, Options Explored (divergent phase summary), Adversarial Testing results, Convergent Analysis scores, Decision, Rationale, Consequences, Validation, Review Schedule.

## AI Execution Instructions

### Tone & Style
- **Clarity**: Simple language, avoid jargon
- **Honesty**: Acknowledge uncertainty and limitations
- **Structure**: Heavy use of headers, tables, bullets
- **Brevity**: Comprehensive but concise

### Quality Gates
- Never skip Stage 1 confirmation
- No proposals with unaddressed fatal flaws
- Scoring must be evidence-based, not arbitrary
- Always show reasoning transparently
- Generate both recommendation AND ADR documentation

### Interaction Model
- **User Control**: Always confirm before stage transitions
- **Flexibility**: User can request deeper dives or pivots
- **Iteration**: Welcome feedback and refinement at any stage

### Error Handling
- **Vague requirements** → More clarification questions (Stage 1)
- **All proposals flawed** → Reframe problem or expand constraints
- **Close scoring** → Explain tie-breaking logic transparently
- **New information** → Restart from Stage 1 without resistance
