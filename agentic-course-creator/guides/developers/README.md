# Developer Guides

**Customizing and Extending the Agentic Course Creator**

---

## Guide Index

| Guide | Purpose | Audience |
|-------|---------|----------|
| [system-architecture.md](system-architecture.md) | Understand how agents work together | All developers |
| [personality-customization.md](personality-customization.md) | Customize agent voice and tone | Content customizers |
| [scoring-rubrics.md](scoring-rubrics.md) | Modify quality scoring rules | Quality engineers |
| [adding-agents.md](adding-agents.md) | Create new specialized agents | System extenders |
| [integration-guide.md](integration-guide.md) | Connect to LMS and external systems | Integration developers |
| [troubleshooting.md](troubleshooting.md) | Debug common issues | All developers |

---

## Quick Start

### 1. Understand the Architecture

```
Course Config → Orchestrator → Specialized Agents → QA Review → Output
```

Each agent has:
- **Soul/North Star**: Core purpose that guides decisions
- **Personality Profile**: Voice, tone, traits
- **Scoring Rubric**: Quality rules with point values
- **Reflection Process**: Self-validation before output

### 2. Common Customization Paths

| Goal | Start Here |
|------|-----------|
| Change agent voice/tone | [personality-customization.md](personality-customization.md) |
| Adjust quality standards | [scoring-rubrics.md](scoring-rubrics.md) |
| Add domain-specific agent | [adding-agents.md](adding-agents.md) |
| Export to different platform | [integration-guide.md](integration-guide.md) |

### 3. Development Workflow

```
1. Modify agent prompt (markdown file)
2. Test with single module generation
3. Review output against scoring rubric
4. Iterate until quality threshold met
5. Deploy to full workflow
```

---

## Key Concepts

### Agent Format v2.0

All agents follow a consistent structure:

```yaml
# Identity
agent_id: unique-identifier
name: "Human-readable name"
role: "What this agent does"
version: 2.0.0

# Soul - The "Why"
soul:
  north_star: "Ultimate purpose"
  core_belief: "Fundamental conviction"
  success_measure: "How to know you've succeeded"
  when_in_doubt: "Default decision guide"

# Personality - The "How"
personality:
  archetype: "Character type"
  energy_baseline: 0-10
  core_traits: [...]
  voice_patterns: {...}

# Scoring - Quality Rules
scoring:
  major_positives: [...] # +10 to +20
  moderate_positives: [...] # +5 to +9
  minor_positives: [...] # +1 to +4
  major_negatives: [...] # -10 to -20
  moderate_negatives: [...] # -5 to -9
  minor_negatives: [...] # -1 to -4
  thresholds:
    minimum_acceptable: 80
    excellent: 100

# Reflection - Self-Validation
reflection:
  design_principles: [...]
  self_scoring:
    minimum_to_proceed: 80
```

### Time Equivalence Principle

All problem set tiers target ~45 minutes. Difficulty varies through scaffolding, not scope.

### CORE + FLEX Model

- **CORE**: 4 lessons per module (Captivate, Orient, Realize, Execute)
- **FLEX**: Tiered problem sets (Foundation, Standard, Advanced, Hacker)

---

## Getting Help

- **Technical Issues**: Check [troubleshooting.md](troubleshooting.md)
- **Feature Requests**: Open GitHub issue
- **Architecture Questions**: Start with [system-architecture.md](system-architecture.md)
