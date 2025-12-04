# Agentic Course Creator (ACC)

**A Demonstration of AMCD Implementation Through AI Agents**

**Status:** Exploratory Reference | **Version:** 1.2.0

---

## What This Is

The Agentic Course Creator is a **supporting demonstration asset** for the [Adaptive Modular Course Design (AMCD)](../papers/adaptive-modular-course-design.md) methodology. It is **not** a finished product, automation tool, or production-ready system.

### This Directory Contains

- **Agent specifications** that illustrate how AMCD principles could be operationalized through AI
- **Persona definitions** showing how the four CORE voices can be systematized
- **Quality rubrics** demonstrating scoring approaches for generated content
- **Workflow documentation** outlining potential orchestration patterns

### This Directory Does Not Contain

- Working code or executable systems
- Production-ready implementations
- Turnkey solutions for automated course generation
- Complete technical specifications for developers

---

## Purpose

The ACC serves three purposes within this repository:

### 1. Demonstration

The agent specifications show that AMCD's principles are concrete enough to guide AI content generation. The persona definitions, scoring rubrics, and structural requirements translate abstract pedagogy into actionable instructions.

**Example**: The lesson-captivate-v2.md agent specification includes:
- Soul/North Star statement defining the agent's purpose
- Personality profile with specific traits and intensities
- Scoring rubric with point values for specific behaviors
- Reflection process for self-evaluation

This level of detail demonstrates that AMCD's voice framework is implementable, not merely theoretical.

### 2. Research Companion

The specifications explore how symbolic rubrics, instruction styles, and structured lesson archetypes interact with AI-assisted content creation. They raise and partially answer questions like:
- Can distinct teaching voices be reliably generated?
- How should quality be measured for educational content?
- What level of specification produces consistent results?

### 3. Open-Core Reference

For those who may build implementations in the future, these specifications provide high-level guidance. They are intentionally incomplete—designed to inform architecture decisions, not to be copied verbatim into production systems.

---

## Directory Structure

```
agentic-course-creator/
├── README.md                    # This file
├── agents/
│   ├── AGENT-FORMAT-V2.md       # Agent specification template
│   ├── orchestrator.md          # Coordination patterns (conceptual)
│   ├── content/
│   │   ├── lesson-captivate-v2.md   # Lesson 1 agent (v2 format)
│   │   ├── lesson-orient-v2.md      # Lesson 2 agent (v2 format)
│   │   ├── lesson-realize-v2.md     # Lesson 3 agent (v2 format)
│   │   ├── lesson-execute-v2.md     # Lesson 4 agent (v2 format)
│   │   └── [v1 agents - legacy]
│   ├── problem-sets/
│   │   └── tier-generator-v2.md     # FLEX problem set generation
│   ├── structure/
│   │   └── course-architect.md      # Course structure planning
│   ├── quality/
│   │   ├── content-reviewer.md      # Quality review patterns
│   │   └── course-assessor.md       # Compliance scoring
│   ├── research/
│   │   └── topic-researcher.md      # Domain research guidance
│   └── adaptation/
│       └── workshop-adapter.md      # Format adaptation
├── guides/developers/           # Technical reference documentation
├── workflows/
│   └── full-course-workflow.md  # End-to-end process outline
└── config/                      # Parameter schemas (planned)
```

---

## Agent Format (v2)

The v2 agent specifications use a structured format that includes:

### Soul / North Star
```yaml
soul:
  north_star: "The agent's ultimate purpose in one sentence"
  core_belief: "What the agent believes about its domain"
  success_measure: "How the agent knows it succeeded"
  when_in_doubt: "Default behavior under uncertainty"
```

### Personality Profile
```yaml
personality:
  archetype: "The agent's teaching persona"
  energy_baseline: 7  # 1-10 scale
  core_traits:
    - trait: "Specific characteristic"
      expression: "How it manifests"
      intensity: 8  # 1-10 scale
```

### Scoring Rubric
```yaml
scoring:
  major_positives:   # +10 to +20 points
  moderate_positives: # +5 to +9 points
  minor_positives:   # +1 to +4 points
  major_negatives:   # -10 to -20 points
  moderate_negatives: # -5 to -9 points
  minor_negatives:   # -1 to -4 points
  thresholds:
    minimum_acceptable: 80
```

This format makes quality criteria explicit and measurable, supporting both human review and automated scoring.

---

## The Four CORE Agents

Each CORE lesson type has a dedicated agent with distinct characteristics:

| Agent | Persona | Energy | Primary Focus |
|-------|---------|--------|---------------|
| **Captivate** | The Enthusiastic Storyteller | 7/10 | Hook, relevance, curiosity |
| **Orient** | The Patient Systematizer | 5/10 | Clarity, examples, progression |
| **Realize** | The Empathetic Navigator | 6/10 | Story, human impact, connection |
| **Execute** | The Focused Coach | 4/10 | Direction, practice, results |

These personas reflect how skilled educators naturally shift their approach based on instructional goals. The specifications make this pattern explicit and reproducible.

---

## Intended Outcomes (Design Goals)

The ACC specifications are designed to address common weaknesses in AI-generated educational content:

| Problem | Design Response |
|---------|-----------------|
| Generic, interchangeable voice | Persona-specific instructions with distinct traits |
| Lack of engagement | Captivate agent focused on hooks and relevance |
| Missing structure | CORE progression enforced across all content |
| Inconsistent quality | Scoring rubrics with explicit criteria |
| No self-evaluation | Reflection process before finalization |

**Note**: These are design goals, not validated outcomes. Whether the specifications achieve these goals in practice requires empirical testing.

---

## What ACC Does Not Do

To set appropriate expectations:

- **Does not run autonomously**: No execution layer exists
- **Does not generate complete courses**: Specifications require orchestration
- **Does not replace expertise**: Human review remains essential
- **Does not guarantee quality**: Output depends on implementation
- **Does not work out-of-the-box**: Integration effort required

If you're looking for a tool to "generate a course," this is not it. If you're exploring how AMCD could be automated, these specifications provide a starting point.

---

## For Future Implementers

If you're considering building on these specifications:

### What's Provided
- Detailed agent personas and behaviors
- Quality rubrics with scoring criteria
- Content structure requirements
- Workflow sequences (conceptual)

### What's Left to You
- Orchestration and coordination logic
- Execution environment and infrastructure
- Integration with LLM APIs
- Quality assurance processes
- Domain-specific customization

### Recommendations
1. **Start with one agent**: Implement lesson-captivate-v2 first
2. **Validate output quality**: Test against the rubric manually
3. **Iterate on specifications**: Adjust based on your domain
4. **Build incrementally**: Don't attempt full orchestration initially

---

## Relationship to AMCD

The ACC exists to demonstrate that AMCD's principles are actionable, not to replace the methodology itself.

**Primary contribution**: The [AMCD methodology](../papers/adaptive-modular-course-design.md)

**Supporting asset**: This ACC specification

Course designers and instructors should focus on understanding AMCD. The ACC is relevant primarily for those interested in AI-assisted content creation research.

---

## Version Notes

**v2 Agents**: The `-v2.md` specifications represent the current format with Soul/North Star, personality profiles, and scoring rubrics.

**v1 Agents**: Earlier specifications without the enhanced format. Retained for reference but v2 is preferred.

---

*The Agentic Course Creator demonstrates how the AMCD methodology could be operationalized. It is exploratory, not production-ready—a reference for future implementation rather than a tool for immediate use.*
