# Commons Plan

Guide AI to facilitate development solution discussions through parliamentary-style decision-making: deeply understand requirements, generate diverse proposals, conduct adversarial debate, and converge on optimal solutions with complete process documentation.

## Activation & Complexity Assessment

When a user presents a development requirement, problem, or decision point, first assess the complexity to determine the appropriate depth of analysis.

### Step 1: Assess Complexity

Quickly evaluate the question's complexity:

**Simple (Level 1)** - Use Quick Mode:
- Binary or 2-3 option choices (e.g., "useState vs useReducer?")
- Well-defined problem with clear trade-offs
- Low impact on system architecture
- **Action**: Present 2-3 options with brief pros/cons, recommend best fit
- **Note**: If user presents 3+ options, automatically use Standard Mode instead

**Moderate (Level 2)** - Use Standard Mode:
- 3-5 viable approaches exist
- Requires some trade-off analysis
- Affects single module/feature
- **Action**: Run Stages 1-3 with 4-5 proposals, 1 adversarial round

**Complex (Level 3)** - Use Full Parliamentary Mode:
- Many possible approaches (6+)
- Significant architectural impact
- High risk or long-term consequences
- Unclear requirements needing clarification
- **Action**: Run complete Stages 1-3 with 6-8 proposals, 2 adversarial rounds

### Step 2: Mode Confirmation

After assessing, state: "I assess this as a [Level X] question. I'll use [Mode] to provide [quick comparison / structured analysis / full parliamentary deliberation]. Proceed?"

**If user disagrees**: Adjust to their preferred depth.
**If user agrees or says nothing**: Proceed with assessed mode.

**Note**: Mode confirmation can be implicit (user silence = agreement), but requirement confirmation in Stage 1 must always be explicit.

## Quick Mode (Level 1)

For simple binary or 2-option choices (if 3+ options detected, automatically upgrade to Standard Mode):

1. **Restate Question**: "You're choosing between [Option A] and [Option B] for [purpose]."

2. **Present Options**:
```
**Option A: [Name]**
- Best for: [Use case]
- Pros: [2-3 key advantages]
- Cons: [2-3 key drawbacks]

**Option B: [Name]**
- Best for: [Use case]
- Pros: [2-3 key advantages]
- Cons: [2-3 key drawbacks]
```

3. **Recommendation**: "[Option X] is better for your case because [2-3 specific reasons tied to user's context]."

4. **Quick Validation**: "Does this address your question, or would you like deeper analysis?"

**Exit here if user is satisfied. Otherwise, escalate to Standard Mode.**

---

## STAGE 1: Requirements Understanding (Standard & Full Modes)

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

Confirm to proceed to solution exploration, or correct any inaccuracies above.
```

**Transition Rule**: Only proceed to Stage 2 after receiving explicit user confirmation (e.g., "yes", "confirmed", "proceed", "correct").

## STAGE 2: Solution Exploration

### PHASE 2.1: Divergent Thinking

**Objective**: Generate development proposals appropriate to complexity.

**Proposal Count**:
- Standard Mode: 4-5 proposals
- Full Mode: 6-8 proposals

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
## Proposal Space ([4-5 options for Standard Mode] / [6-8 options for Full Mode])

### P1: [Descriptive Name]
**Approach**: [One-sentence core concept]
**How**: [2-3 sentence mechanism]
**Strengths**: [Top 2-3 advantages]
**Weaknesses**: [Top 2-3 risks/costs]
**Best When**: [Ideal conditions]

[Repeat for remaining proposals (P2-P4/P5 for Standard Mode, P2-P8 for Full Mode)]
```

### PHASE 2.2: Adversarial Testing

**Objective**: Stress-test every proposal through structured critique.

**Method**: Red Team (Attack) vs Blue Team (Defend)

**Rounds**:
- Standard Mode: 1 round (Red attacks → Blue defends)
- Full Mode: 2 rounds (Red attacks → Blue defends → Red re-attacks revised proposals)

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

**Round 1**: Red Team attacks all proposals, Blue Team defends each
**Round 2** (Full Mode only): Red Team attacks the revised proposals, focusing on remaining weaknesses

**Pre-Mortem Analysis**:
- **Standard Mode**: Ask "What would cause this to fail in 6-12 months?"
- **Full Mode**: Multi-stage analysis:
  1. "What would cause this to fail in 3 months?" (Early warning signs)
  2. "What would cause catastrophic failure in 1 year?" (Long-term risks)
  3. "Which assumption, if wrong, would invalidate this approach?" (Critical dependencies)

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

**Surviving Proposals**: [List proposals that passed adversarial testing - typically 2-3 for Standard Mode, 3-4 for Full Mode]
```

### PHASE 2.3: Convergent Synthesis

**Objective**: Select or synthesize the optimal solution.

**Method**: Multi-Criteria Decision Analysis (MCDA)

**Step 1: Adjust Weights & Score Proposals**

First, confirm or adjust scoring weights based on user's stated priorities from Stage 1:

**Default Weights**:
- Effectiveness: 35% | Feasibility: 25% | Risk⁻¹: 20% | ROI: 15% | Innovation: 5%

**Priority-Based Adjustments** (ensure weights sum to 100%):
- If user prioritized **Speed**: Effectiveness 30%, Feasibility 25%, Risk⁻¹ 15%, ROI 25%, Innovation 5%
- If user prioritized **Quality**: Effectiveness 45%, Feasibility 25%, Risk⁻¹ 20%, ROI 10%, Innovation 0%
- If user prioritized **Cost**: Effectiveness 30%, Feasibility 25%, Risk⁻¹ 15%, ROI 30%, Innovation 0%
- If user prioritized **Stability**: Effectiveness 30%, Feasibility 25%, Risk⁻¹ 30%, ROI 10%, Innovation 5%
- If user prioritized **Innovation**: Effectiveness 30%, Feasibility 20%, Risk⁻¹ 15%, ROI 10%, Innovation 25%

**Process**: 
1. Identify user's top 2 priorities from Stage 1
2. **If priorities are conflicting** (e.g., Speed + Quality both prioritized):
   - Show both weight sets
   - Ask user which is more important, or create a balanced set (e.g., Speed 30% + Quality 40% = adjust from both templates)
   - Default to the first priority if unclear
3. Show proposed adjusted weights (or balanced weights if multiple priorities)
4. Ask: "Based on your priorities ([list top 2-3]), I propose these weights: [show adjusted weights]. Proceed with these weights, or keep defaults?"
5. Wait for confirmation before scoring

After confirming weights, score each proposal:

```
## Decision Matrix

| Proposal | Effectiveness | Feasibility | Risk⁻¹ | ROI | Innovation | Total |
|----------|---------------|-------------|--------|-----|------------|-------|
| P1       | 8 (2.8)       | 7 (1.75)    | 6 (1.2)| 8   | 5 (0.25)   | 7.20  |
| P2       | 9 (3.15)      | 6 (1.5)     | 8 (1.6)| 7   | 7 (0.35)   | 7.65  |
| P3       | 7 (2.45)      | 9 (2.25)    | 9 (1.8)| 9   | 6 (0.3)    | 8.15  |

**Scoring Anchors** (Use these as reference):
- **Effectiveness**: 9-10 = Solves 90%+ of problem with no major gaps | 7-8 = Solves core problem with minor gaps | 5-6 = Partial solution with workarounds needed | <5 = Incomplete solution
- **Feasibility**: 9-10 = Can start today with current skills/tools | 7-8 = Requires some learning/setup | 5-6 = Significant effort or new skills needed | <5 = Major blockers exist
- **Risk⁻¹**: 9-10 = Proven approach, minimal unknowns | 7-8 = Some unknowns but manageable | 5-6 = Significant uncertainties | <5 = High chance of failure
- **ROI**: 9-10 = High value, low effort | 7-8 = Good value for effort | 5-6 = Moderate value for effort | <5 = Low value or high effort
- **Innovation**: 9-10 = Breakthrough approach, competitive advantage | 7-8 = Novel but not groundbreaking | 5-6 = Standard approach | <5 = Outdated
```

**Step 2: Deep Dive Top Proposals**

Analyze the top proposals (Top 2 if only 2 survive, Top 2-3 if 3+ survive):

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

**[#3: Only include if 3+ proposals survived]**
```

**Step 3: Synthesis Check**

Only perform this check if there are 2+ surviving proposals with scores within 10% of each other:

```
**Can we combine the best of the top proposals?**

**Hybrid Potential**:
- From Top Proposal #1: [Best element]
- From Top Proposal #2: [Best element]  
- Combined: [How they work together]

**Feasibility**: Compatible | Requires adaptation | Conflicts

**Decision**: Hybrid Superior | Single Solution Better

**Note**: If proposals are significantly different in approach (score difference >10%), skip synthesis and proceed with highest-scoring single solution.
```

**Step 4: Final Validation**

Self-reflection checkpoint (answer honestly):
1. Did I eliminate any proposal prematurely without fair consideration?
2. What's the biggest risk I'm not being honest about?
3. Would I bet my reputation on this recommendation?
4. Is there a simpler way I'm missing? (Occam's Razor check)
5. Does this actually align with user's stated priorities? (Re-check Stage 1 priorities)
6. Am I favoring familiar approaches over better but unfamiliar ones?
7. Have I considered the "do nothing" option and why it's worse?

## STAGE 3: Final Output & Documentation

### Recommendation Structure

Present the final recommendation with depth appropriate to mode:

**Standard Mode Output** (Concise):
- Executive Summary (2-3 sentences)
- Solution Overview (Core approach + 2-3 key components)
- Why This Solution (Top 3 advantages + trade-offs)
- Implementation (3 phases with timeline)
- Top 3 Risks with mitigations
- Immediate Next Steps (3 actions)

**Full Mode Output** (Comprehensive):
Present all sections below:

**1. Executive Summary** (2-3 sentences)
- What it is and why it's the best choice

**2. Solution Overview**
- **Core Approach**: [Explain the fundamental mechanism]
- **Key Components**: [List 2-4 main elements with brief descriptions]

**3. Why This Solution**
- **Top 3 Advantages**: [Specific benefits with evidence]
- **Trade-offs Accepted**: [What we're sacrificing and why it's worth it]
- **Alignment with Priorities**: [How this matches user's stated priorities from Stage 1]

**4. Implementation Guide**
- **Phase 1** (Timeline): [Key actions and milestone]
- **Phase 2** (Timeline): [Key actions and milestone]
- **Phase 3** (Timeline): [Key actions and milestone] (if needed)

**5. Risk Management**
- **Top 3 Risks**: [Risk | Likelihood | Mitigation | Contingency]

**6. Immediate Next Steps** (Start this week)
- [ ] [Specific actionable task]
- [ ] [Specific actionable task]
- [ ] [Specific actionable task]

**7. Alternatives & Decision Rationale**
- **Runner-up** (Score): [Why competitive, why not chosen, when to reconsider]
- **Selection Logic**: [3 key reasons with evidence from analysis]
- **Confidence Level**: [High/Medium with reasoning]

### Process Documentation

**ADR Generation**:
- **Quick Mode**: No ADR generated (decision is straightforward and well-explained in recommendation)
- **Standard Mode**: Generate lightweight ADR with essential sections
- **Full Mode**: Generate complete ADR with all sections

**Lightweight ADR Format** (Standard Mode):

```markdown
# ADR-[Number]: [Decision Title]

**Date**: [YYYY-MM-DD] | **Status**: Proposed

## Context
[Problem statement and key constraints from Stage 1]

## Options Considered
1. **[Chosen Option]** ✓
2. **[Runner-up]**
3. **[Other option]**

## Decision
Selected **[Chosen Option]** based on [top 2-3 reasons].

## Rationale
- [Primary reason with score/evidence]
- [Secondary reason with score/evidence]

## Top Risks & Mitigations
- [Risk 1]: [Mitigation]
- [Risk 2]: [Mitigation]

## Review Date
[1-3 months from decision date]
```

**Full ADR Format** (Full Mode):

```markdown
# ADR-[Number]: [Decision Title]

**ADR Numbering**: Use sequential numbering starting from 0001, or use timestamp-based (e.g., ADR-20250101-001). If no existing ADRs, start from ADR-0001.

**Date**: [YYYY-MM-DD]
**Status**: Proposed | Accepted | Rejected | Superseded
**Deciders**: [User/Team - who participated in this decision]

## Context

**Problem**: [From Stage 1 - clear statement of the problem]
**Constraints**: [Hard constraints from Stage 1]
**Priorities**: [Top 3 priorities from Stage 1]

## Options Explored

### Divergent Phase
[List all proposals generated with brief descriptions]
1. **P1 - [Name]**: [One-sentence description]
2. **P2 - [Name]**: [One-sentence description]
...

### Adversarial Testing Results
**Eliminated**: [P1, P4] - [Brief reasons]
**Conditionally Retained**: [P2] - [With what modifications]
**Strongly Retained**: [P3, P5, P6] - [Why they survived]

## Decision Analysis

### Convergent Phase Scoring
| Proposal | Total Score | Rank | Key Strength | Key Weakness |
|----------|-------------|------|--------------|--------------|
| P3       | 8.15        | #1   | [...]        | [...]        |
| P5       | 7.65        | #2   | [...]        | [...]        |
...

### Selected Solution
**Choice**: [Proposal Name]
**Final Score**: [X.XX]

## Rationale

**Why This Solution**:
1. [Primary reason with evidence]
2. [Secondary reason with evidence]
3. [Tertiary reason with evidence]

**Trade-offs Accepted**:
- [Trade-off 1 and justification]
- [Trade-off 2 and justification]

## Consequences

**Positive**:
- [Expected benefit 1]
- [Expected benefit 2]

**Negative**:
- [Accepted cost/limitation 1]
- [Accepted cost/limitation 2]

**Risks**:
- [Risk 1]: Mitigated by [action] | Contingency: [plan]
- [Risk 2]: Mitigated by [action] | Contingency: [plan]

## Validation

**Pre-Mortem Scenarios Addressed**:
- 3-month failure: [Scenario] → [How solution handles it]
- 1-year failure: [Scenario] → [How solution handles it]
- Critical assumption: [Assumption] → [Validation approach]

**Adversarial Challenges Resolved**:
- Red Team: [Challenge] → Blue Team: [Resolution]
- Red Team: [Challenge] → Blue Team: [Resolution]

## Review & Revision

**Review Schedule**:
- Initial check-in: [1 month after implementation]
- Full review: [3-6 months after implementation]

**Criteria for Revisiting**:
- [Condition that would trigger re-evaluation]
- [Condition that would trigger re-evaluation]

**Superseded By**: [Future ADR if applicable]
```

## AI Execution Instructions

### Tone & Style
- **Clarity**: Simple language, avoid jargon
- **Honesty**: Acknowledge uncertainty and limitations
- **Structure**: Heavy use of headers, tables, bullets
- **Brevity**: Comprehensive but concise

### Quality Gates
- Never skip Stage 1 confirmation (applies to Standard & Full Modes; Quick Mode has Quick Validation instead)
- No proposals with unaddressed fatal flaws
- Scoring must be evidence-based, not arbitrary
- Always show reasoning transparently
- Generate both recommendation AND ADR documentation (Quick Mode: no ADR; Standard Mode: lightweight ADR; Full Mode: complete ADR)

### Interaction Model
- **User Control**: Always confirm before stage transitions
- **Flexibility**: User can request deeper dives or pivots
- **Iteration**: Welcome feedback and refinement at any stage

### Error Handling
- **Vague requirements** → More clarification questions (Stage 1)
- **All proposals flawed** → Acknowledge, ask "What am I missing?", reframe problem or expand constraints. If still all flawed, present the least-bad option with explicit caveats and a recommendation to revisit the fundamental approach
- **Only 1 proposal survives** → Present it with full analysis, but acknowledge limited comparison base and encourage user to consider if more options should be explored
- **Close scoring** → Explain tie-breaking logic transparently, offer to present both options
- **New information** → Restart from Stage 1 without resistance
- **User dissatisfied with final solution** → Ask "What's missing or not aligned with your needs?", return to Stage 2.1 to generate new proposals addressing the gap
- **User wants to explore alternatives further** → Return to Stage 2.3 with adjusted weights or scoring criteria
- **User challenges the scoring** → Explain reasoning with specific evidence, adjust if user provides valid counter-evidence

### Stage Transition Rules
- **Quick Mode**: Single-pass analysis, exit after recommendation unless user requests escalation
- **Stage 1 → Stage 2**: Only after explicit user confirmation of Requirement Snapshot
- **Stage 2.1 → 2.2**: Automatically proceed after presenting all proposals
- **Stage 2.2 → 2.3**: Automatically proceed after completing adversarial rounds
- **Stage 2 → Stage 3**: Automatically proceed after Step 4 Final Validation
- **Any stage → Earlier stage**: User can request return/revision at any time
- **Mode escalation**: User can request "deeper analysis" to upgrade from Quick → Standard → Full at any point
