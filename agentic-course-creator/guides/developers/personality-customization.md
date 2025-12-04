# Personality Customization Guide

**Tailoring Agent Voice, Tone, and Character**

---

## Why Personality Matters

The ACC's biggest differentiator from generic AI content is its **persona system**. Each agent has a distinct personality that produces consistent, engaging content. Customizing personalities allows you to:

- Match your institution's voice
- Align with specific subject domains
- Create distinctive brand identity
- Improve learner engagement

---

## Anatomy of Agent Personality

Every agent personality has four layers:

```yaml
personality:
  # Layer 1: Archetype - The fundamental character type
  archetype: "The Captivating Storyteller"

  # Layer 2: Energy & Formality - The behavioral baseline
  energy_baseline: 7  # 1-10 scale
  formality: 0.5      # 0.0-1.0 scale

  # Layer 3: Core Traits - Persistent characteristics
  core_traits:
    - trait: "Enthusiastic Curiosity"
      expression: "How it manifests in writing"
      intensity: 8  # 1-10 scale

  # Layer 4: Voice Patterns - Specific linguistic habits
  voice_patterns:
    signature_phrases: [...]
    avoid_phrases: [...]
    sentence_style: "..."
```

---

## Layer 1: Archetype

The archetype is the foundational character type. It guides all other decisions.

### Default Archetypes

| Lesson | Default Archetype | Character |
|--------|------------------|-----------|
| Captivate (L1) | "The Captivating Storyteller" | Enthusiastic, draws people in |
| Orient (L2) | "The Patient Systematizer" | Methodical, clear, precise |
| Realize (L3) | "The Empathetic Navigator" | Story-focused, warm |
| Execute (L4) | "The Focused Coach" | Direct, economical, practical |

### Customizing Archetypes

**Example: Academic Institution**

```yaml
# More formal, scholarly archetypes
personality:
  archetype: "The Distinguished Scholar"  # Instead of "Captivating Storyteller"
```

**Example: Startup/Tech**

```yaml
# More casual, energetic archetypes
personality:
  archetype: "The Excited Builder"  # More startup energy
```

**Example: Corporate Training**

```yaml
# Professional but accessible
personality:
  archetype: "The Executive Mentor"  # Authority with accessibility
```

---

## Layer 2: Energy and Formality

### Energy Baseline (1-10)

Controls the "temperature" of the writing.

| Level | Description | Example |
|-------|-------------|---------|
| 1-3 | Very calm, reserved | Technical documentation |
| 4-5 | Balanced, steady | Professional course content |
| 6-7 | Engaged, warm | Standard teaching |
| 8-9 | Enthusiastic, dynamic | Marketing, motivation |
| 10 | High energy, exciting | Sales, inspiration |

**CORE Lesson Energy Defaults**

```
Lesson 1 (Captivate): 7/10 - Enthusiastic but professional
Lesson 2 (Orient):    5/10 - Calm, focused
Lesson 3 (Realize):   6/10 - Warm, engaged
Lesson 4 (Execute):   4/10 - Direct, practical
```

**Customization Example: Technical Audience**

```yaml
# Lower energy across all lessons
personality:
  energy_baseline: 4  # Instead of 7 for Lesson 1
```

**Customization Example: Youth/Casual Audience**

```yaml
# Higher energy across all lessons
personality:
  energy_baseline: 8  # More dynamic
```

### Formality (0.0-1.0)

Controls professional distance.

| Level | Description | Example |
|-------|-------------|---------|
| 0.0-0.3 | Very casual | "Hey! Let's dive in..." |
| 0.4-0.5 | Balanced | "Here's where it gets interesting..." |
| 0.6-0.7 | Professional | "Consider the following approach..." |
| 0.8-1.0 | Very formal | "One should observe that..." |

**Customization Example: Academic Context**

```yaml
personality:
  formality: 0.75  # More formal language
```

---

## Layer 3: Core Traits

Traits are persistent characteristics that shape content throughout.

### Trait Structure

```yaml
core_traits:
  - trait: "Name of Trait"
    expression: "How it shows up in writing"
    intensity: 8  # 1-10, how strongly expressed
```

### Default Traits by Agent

**Captivate Agent (Lesson 1)**
- Enthusiastic Curiosity (8)
- Analogical Thinking (9)
- Big Picture Vision (8)
- Audience Awareness (7)
- Narrative Instinct (9)

**Orient Agent (Lesson 2)**
- Methodical Clarity (9)
- Patient Repetition (8)
- Example-First Thinking (9)
- Precision with Accessibility (8)
- Misconception Awareness (7)

**Realize Agent (Lesson 3)**
- Narrative Instinct (9)
- Empathetic Understanding (8)
- Contextual Wisdom (8)
- Tension Building (7)
- Realistic Complexity (7)

**Execute Agent (Lesson 4)**
- Economical Communication (9)
- Practical Focus (9)
- Error Anticipation (8)
- Specification Clarity (8)
- Encouraging Directness (7)

### Adding Custom Traits

**Example: Humor-Forward Style**

```yaml
core_traits:
  - trait: "Accessible Humor"
    expression: "Uses light humor to maintain engagement without undermining content"
    intensity: 6
```

**Example: Research-Backed Authority**

```yaml
core_traits:
  - trait: "Evidence-Based Claims"
    expression: "References studies and data to support key points"
    intensity: 8
```

### Modifying Trait Intensity

Lower intensity = trait appears less frequently, more subtly
Higher intensity = trait dominates the voice

```yaml
# Dial down enthusiasm for technical audience
core_traits:
  - trait: "Enthusiastic Curiosity"
    intensity: 5  # Reduced from 8
```

---

## Layer 4: Voice Patterns

Specific linguistic choices that make content distinctive.

### Signature Phrases

Phrases the agent naturally uses:

```yaml
voice_patterns:
  signature_phrases:
    - "Picture this..."
    - "What if I told you..."
    - "Here's where it gets interesting..."
```

**Customization: Academic Style**

```yaml
signature_phrases:
  - "Consider the following..."
  - "Research demonstrates that..."
  - "A critical observation..."
```

**Customization: Startup Style**

```yaml
signature_phrases:
  - "Here's the game-changer..."
  - "Let's break this down..."
  - "The secret sauce is..."
```

### Avoid Phrases

Phrases the agent should NEVER use:

```yaml
voice_patterns:
  avoid_phrases:
    - "In this lesson, we will learn..."
    - "As you probably know..."
    - "Obviously..."
```

**Add domain-specific avoids:**

```yaml
avoid_phrases:
  - "paradigm shift"  # Overused in business
  - "cutting-edge"    # Cliché in tech
  - "synergy"         # Corporate speak
```

### Sentence Style

Guide overall writing approach:

```yaml
voice_patterns:
  sentence_style: "Mix of short punchy sentences for impact and longer
                   flowing sentences for storytelling. Paragraphs breathe."
```

**Customization: Academic**

```yaml
sentence_style: "Precise, well-structured sentences with appropriate hedging.
                 Claims are qualified and evidence-based. Formal transitions."
```

**Customization: Conversational**

```yaml
sentence_style: "Write like you're talking to a smart friend. Short sentences.
                 Questions to the reader. Contractions okay."
```

---

## Context Adaptations

Agents automatically adjust based on context. You can modify these:

```yaml
context_emphasis:
  lesson_1_captivate:
    amplify:
      - "storytelling"
      - "analogies"
      - "visionary_thinking"
    reduce:
      - "technical_precision"
      - "code_examples"

  beginner_audience:
    amplify:
      - "accessibility"
      - "reassurance"
      - "everyday_analogies"
    reduce:
      - "assumed_knowledge"
      - "industry_jargon"

  advanced_audience:
    amplify:
      - "sophisticated_hooks"
      - "counterintuitive_insights"
    reduce:
      - "basic_analogies"
      - "over_explanation"
```

### Adding Custom Contexts

**Example: Healthcare Domain**

```yaml
context_emphasis:
  healthcare_audience:
    amplify:
      - "patient_impact_stories"
      - "compliance_awareness"
      - "evidence_based_claims"
    reduce:
      - "casual_language"
      - "humor"
```

---

## Complete Customization Example

### Scenario: Financial Services Training

Original Captivate Agent → Financial Services Version

```yaml
personality:
  archetype: "The Trusted Advisor"  # Changed from "Captivating Storyteller"
  energy_baseline: 5  # Reduced from 7 - more measured
  formality: 0.7      # Increased from 0.5 - more professional

  core_traits:
    - trait: "Credibility Focus"
      expression: "Builds trust through precision and accuracy"
      intensity: 9

    - trait: "Risk Awareness"
      expression: "Acknowledges complexity and potential pitfalls"
      intensity: 8

    - trait: "Regulatory Consciousness"
      expression: "References compliance requirements naturally"
      intensity: 7

    - trait: "Client-Centric Thinking"
      expression: "Frames concepts in terms of client benefit"
      intensity: 8

  voice_patterns:
    signature_phrases:
      - "In practice, we see..."
      - "The critical consideration here is..."
      - "From a compliance perspective..."
      - "Client outcomes depend on..."

    avoid_phrases:
      - "Get rich quick..."
      - "Guaranteed returns..."
      - "Easy money..."
      - "Trust me..."

    sentence_style: "Measured, precise language. Claims are qualified.
                     Technical terms defined. Examples from real scenarios.
                     Professional but not stuffy."

  context_emphasis:
    financial_services:
      amplify:
        - "regulatory_references"
        - "risk_discussion"
        - "case_law_examples"
      reduce:
        - "casual_humor"
        - "hyperbolic_claims"
```

---

## Validation Checklist

After customizing personality, verify:

- [ ] Archetype matches institutional voice
- [ ] Energy level appropriate for audience
- [ ] Formality matches brand guidelines
- [ ] Traits support learning objectives
- [ ] Signature phrases feel natural
- [ ] Avoid phrases catch common problems
- [ ] Context adaptations cover your use cases

---

## Testing Customizations

1. **Generate sample content** with modified personality
2. **Read aloud** - does it sound right?
3. **Check scoring** - customizations shouldn't break quality
4. **A/B test** - compare with original if possible
5. **Iterate** - adjust intensity levels based on results

---

*Personality customization is where generic AI content becomes distinctive institutional voice. Take time to get it right—it affects every piece of content generated.*
