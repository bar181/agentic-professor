# Scoring Rubrics Guide

**Customizing Quality Standards and Thresholds**

---

## How Scoring Works

Every agent uses a point-based scoring system to ensure consistent quality. Understanding and customizing these rubrics lets you enforce your institution's standards.

### Scoring Categories

```yaml
scoring:
  major_positives:    # +10 to +20 points - Critical quality indicators
  moderate_positives: # +5 to +9 points  - Important but not critical
  minor_positives:    # +1 to +4 points  - Nice to have
  major_negatives:    # -10 to -20 points - Serious issues
  moderate_negatives: # -5 to -9 points  - Problems to fix
  minor_negatives:    # -1 to -4 points  - Minor concerns

  thresholds:
    minimum_acceptable: 80  # Below this = regenerate or flag
    good: 90               # Target quality
    excellent: 100         # Exceptional output
```

### Score Calculation

1. Start with baseline of 0
2. Add points for each positive behavior present
3. Subtract points for each negative behavior present
4. Compare against thresholds

---

## Understanding Existing Rubrics

### Captivate Agent (Lesson 1) - Key Scoring

| Behavior | Points | Why |
|----------|--------|-----|
| Opens with emotionally resonant hook | +20 | First impression is critical |
| Uses unexpected analogy | +15 | Memorable connections |
| Establishes clear stakes | +15 | Relevance drives engagement |
| Opens with "In this lesson we will learn..." | -20 | Textbook opening kills engagement |
| Includes implementation code | -15 | Wrong lesson for code |
| Uses undefined jargon | -12 | Barriers to entry |

### Orient Agent (Lesson 2) - Key Scoring

| Behavior | Points | Why |
|----------|--------|-----|
| Each concept has definition, importance, mechanism | +15 | Complete understanding |
| Provides 2-3 progressive examples | +15 | Building complexity |
| Addresses common misconception | +12 | Prevents confusion |
| No examples (abstract only) | -20 | Inaccessible |
| Code without comments | -15 | Unexplained code is a puzzle |
| Uses undefined jargon | -12 | Comprehension barrier |

### Realize Agent (Lesson 3) - Key Scoring

| Behavior | Points | Why |
|----------|--------|-----|
| Opens in medias res | +15 | Immediate engagement |
| Hero faces genuine dilemma | +15 | Real decisions aren't obvious |
| Connects to Lesson 2 concepts | +12 | Theory in action |
| No named hero character | -15 | Stories need protagonists |
| Reads like documentation | -20 | Must be narrative |
| Solution appears obvious | -12 | No tension = no learning |

### Execute Agent (Lesson 4) - Key Scoring

| Behavior | Points | Why |
|----------|--------|-----|
| Task has single, clear deliverable | +15 | Ambiguity causes frustration |
| Includes testable success criteria | +15 | Self-verification |
| Shows common error with explanation | +12 | Prevent predictable mistakes |
| Task is vague | -20 | Unclear tasks cause anxiety |
| No success criteria | -15 | Cannot self-assess |
| Long theoretical explanation | -12 | Wrong lesson for theory |

---

## Customizing Rubrics

### Adding New Behaviors

**Example: Compliance Requirement**

```yaml
major_positives:
  - action: "Includes regulatory reference when applicable"
    points: +12
    rationale: "Financial services courses require compliance awareness"

major_negatives:
  - action: "Makes unqualified claims about outcomes"
    points: -15
    rationale: "Compliance violation in regulated industries"
```

### Adjusting Point Values

**Example: Emphasizing Accessibility**

```yaml
# Increase penalties for accessibility barriers
major_negatives:
  - action: "Uses undefined acronym"
    points: -10  # Increased from -5
    rationale: "Accessibility is critical for our audience"
```

### Changing Thresholds

**Example: Higher Standards**

```yaml
thresholds:
  minimum_acceptable: 85  # Up from 80
  good: 95               # Up from 90
  excellent: 100
```

**Example: Lower Standards for Rapid Drafts**

```yaml
thresholds:
  minimum_acceptable: 70  # Lower for first drafts
  good: 80
  excellent: 90
```

---

## Domain-Specific Rubrics

### Healthcare Training

```yaml
scoring:
  major_positives:
    - action: "Includes patient safety consideration"
      points: +15
      rationale: "Healthcare must prioritize safety"

    - action: "References evidence-based practice"
      points: +12
      rationale: "Healthcare requires evidence basis"

  major_negatives:
    - action: "Provides medical advice without disclaimers"
      points: -20
      rationale: "Liability and accuracy concerns"

    - action: "Uses outdated treatment protocols"
      points: -15
      rationale: "Medical accuracy is non-negotiable"
```

### Software Engineering

```yaml
scoring:
  major_positives:
    - action: "Code examples are runnable and tested"
      points: +15
      rationale: "Broken code destroys credibility"

    - action: "Includes error handling patterns"
      points: +10
      rationale: "Real code needs error handling"

  major_negatives:
    - action: "Security vulnerability in code example"
      points: -20
      rationale: "Cannot teach insecure practices"

    - action: "Deprecated API or library usage"
      points: -12
      rationale: "Outdated code causes confusion"
```

### Business/Leadership

```yaml
scoring:
  major_positives:
    - action: "Includes real company case study"
      points: +15
      rationale: "Business learners want real examples"

    - action: "Addresses implementation challenges"
      points: +10
      rationale: "Theory without practice is academic"

  major_negatives:
    - action: "Uses buzzwords without substance"
      points: -12
      rationale: "Business audience detects fluff"

    - action: "Ignores resource/budget constraints"
      points: -10
      rationale: "Impractical advice is useless"
```

---

## Scoring for Problem Sets

### Tier-Specific Scoring

```yaml
tier_1_scoring:
  major_positives:
    - action: "Step-by-step guidance with checkpoints"
      points: +15
    - action: "Expected outputs shown explicitly"
      points: +12

tier_3_scoring:
  major_positives:
    - action: "Requirements only, no hints"
      points: +15
    - action: "Requires independent design decisions"
      points: +12

  major_negatives:
    - action: "Includes hints or guidance"
      points: -12
      rationale: "Advanced tier should require independence"
```

---

## Threshold Behavior

### What Happens at Each Threshold

| Score | System Behavior |
|-------|-----------------|
| ≥ 90 | Auto-approve, proceed |
| 80-89 | Auto-apply minor revisions, then approve |
| 70-79 | Regenerate with feedback |
| < 70 | Flag for human review |

### Customizing Threshold Actions

```yaml
threshold_actions:
  above_90:
    action: "approve"
    human_review: false

  between_80_90:
    action: "revise_and_approve"
    revisions: ["minor_improvements"]
    human_review: false

  between_70_80:
    action: "regenerate"
    feedback: "Use reviewer suggestions"
    max_attempts: 3
    human_review_on_failure: true

  below_70:
    action: "halt"
    human_review: true
    notify: ["content_team@institution.edu"]
```

---

## Quality Metrics Dashboard

Track scoring over time:

```yaml
quality_metrics:
  aggregate:
    average_score: 91.3
    below_threshold_rate: 2.1%
    regeneration_rate: 5.4%

  by_lesson_type:
    captivate: 93.2
    orient: 90.1
    realize: 89.8
    execute: 92.0

  common_deductions:
    - behavior: "Word count outside range"
      frequency: 12%
      average_deduction: -3

    - behavior: "Missing checkpoint verification"
      frequency: 8%
      average_deduction: -5
```

---

## Best Practices

### When Adjusting Scores

1. **Don't over-weight single behaviors** - No single item should dominate
2. **Balance positives and negatives** - Both should add up similarly
3. **Test with real content** - Generate, score, review results
4. **Document your rationale** - Future maintainers need context

### When Changing Thresholds

1. **Start conservative** - It's easier to lower standards than raise them
2. **Monitor regeneration rates** - High rates = thresholds may be too strict
3. **Review flagged content** - Understand why things fail
4. **Adjust incrementally** - 5 points at a time

---

*Scoring rubrics are the quality backbone of the ACC. Customize them thoughtfully to reflect your institution's actual standards, not aspirational ones.*
