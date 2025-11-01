# Commons Plan

A rigorous AI system prompt for **development solution discussions**, inspired by parliamentary decision-making. Transform vague requirements into optimal development solutions through structured collective deliberation and debate.

Use this system to facilitate thoughtful, debate-driven discussions about technical choices, architecture decisions, and implementation strategies.

## What It Does

Commons Plan guides AI through a **three-stage parliamentary-style process for development solution discussions**:

1. **Requirements Understanding** - Public hearings and iterative clarification until 100% clarity on development needs
2. **Solution Exploration** - Generate diverse development proposals → Adversarial debate → Convergent voting
3. **Documentation** - Complete legislative record of the development decision with rationale

## Why It's Different

Most AI tools jump straight to development solutions. Commons Plan emulates parliamentary deliberation for technical decision-making:

- **Clarifies first** - Never assumes, always confirms
- **Explores broadly** - Generates 6-8 fundamentally different approaches
- **Challenges rigorously** - Red team critiques every solution
- **Decides systematically** - Multi-criteria weighted scoring
- **Documents completely** - Full legislative record (ADR format)

## Core Methodology

Built on research-backed frameworks:

- **Chain-of-Thought Reasoning** - Step-by-step logical progression
- **Adversarial Collaboration** - Red team / Blue team critique
- **Pre-Mortem Analysis** - Identify failures before they happen
- **Multi-Criteria Decision Analysis** - Weighted scoring across dimensions
- **Architecture Decision Records** - Complete traceability

## Process Flow

```
User Input 
    ↓
Clarification Loop (2-3 rounds)
    ↓
Divergent Generation (6-8 diverse solutions)
    ↓
Adversarial Debate (Red team vs Blue team)
    ↓
Convergent Synthesis (MCDA scoring → Selection)
    ↓
Final Recommendation + ADR Documentation
```

## Use Cases

Perfect for development solution discussions:

- **Technology choices** - Which framework/library to adopt?
- **Architecture decisions** - Which system design pattern?
- **Implementation strategies** - Which approach to build the feature?
- **Development trade-offs** - Performance vs maintainability vs speed
- **Team debates** - Structured discussion of competing proposals

## Example Session: Development Solution Discussion

**User**: "I need to improve my app's performance"

**AI** (Parliamentary-style deliberation):
```
I understand your requirement as:
**Problem**: App performance is suboptimal
**Goal**: Improve performance
**Context**: [Needs clarification]

To ensure clarity, could you clarify:
1. What specific performance issue? (load time/responsiveness/crashes)
2. Current metrics and target metrics?
3. Constraints? (budget/time/can't rewrite)
```

[After clarification...]

**AI** generates:
- 6-8 diverse proposals (caching, CDN, code optimization, architecture change...)
- Red team debates and critiques each proposal
- Scores all proposals across effectiveness/feasibility/risk/ROI
- Recommends optimal solution with full rationale
- Documents entire deliberation process in legislative record format (ADR)

## Key Features

### Never Skips Understanding
Enforces confirmation gate before solution generation.

### True Diversity
Solutions span: Conservative | Innovative | Minimal | Scalable | Cost-Optimized | Speed-Optimized | Quality-Optimized | Hybrid

### Adversarial Rigor
Every solution faces:
- Fatal flaw identification
- Assumption challenges  
- Pre-mortem failure scenarios
- Hidden complexity exposure

### Evidence-Based Selection
Multi-criteria scoring with:
- Customizable weights based on priorities
- Transparent rationale for every score
- Synthesis check for hybrid solutions

### Complete Traceability
Generates ADR documenting:
- All options explored
- Why each was eliminated/retained
- Trade-offs accepted
- Decision rationale
- Review schedule

## Quality Guarantees

The prompt includes self-checks:

- Never skip Stage 1 confirmation
- No solutions with unaddressed fatal flaws
- No arbitrary scoring without evidence
- Always show reasoning transparently
- Generate both recommendation AND documentation

## Optimization

Designed for:
- **Clarity** - Simple language, structured format
- **Rigor** - No shortcuts, complete analysis
- **Efficiency** - Streamlined process (5-7 rounds)
- **Transparency** - All reasoning visible
- **Actionability** - Immediate next steps included

## Credits

Built on research-backed methods:

- **Chain-of-Thought Prompting**: Wei et al. (2022). "Chain-of-Thought Prompting Elicits Reasoning in Large Language Models." https://arxiv.org/abs/2201.11903

- **Red Team / Blue Team Adversarial Critique**: Standard military and cybersecurity practice for structured adversarial analysis

- **Pre-Mortem Analysis**: Klein, G. (2007). "Performing a Project Premortem." Harvard Business Review, September 2007. https://hbr.org/2007/09/performing-a-project-premortem

- **ATAM (Architecture Tradeoff Analysis Method)**: CMU Software Engineering Institute. https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=513908

- **ADR (Architecture Decision Records)**: Nygard, M. (2011). "Documenting Architecture Decisions." http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions