# Adaptive Modular Course Design (AMCD)

> *A research-backed instructional design methodology for scalable, adaptable course creation—with an exploratory AI implementation concept.*

**A Research-Informed Framework for Designing Scalable Technical Education**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-2.0.0-green.svg)](CHANGELOG.md)

---

## Purpose of This Repository

This repository presents the **Adaptive Modular Course Design (AMCD)** methodology—a research-informed instructional framework for designing high-quality technical education with consistency, adaptability, and pedagogical rigor.

**AMCD is the core contribution.**

It establishes a repeatable process for designing and scaling course content while maintaining instructional integrity across audiences, delivery formats, and instructional teams.

> **Note:** This is an original course design framework synthesizing established pedagogical principles (Bloom's taxonomy, cognitive load theory, Vygotsky's scaffolding, narrative pedagogy, and others). It does not reproduce or include any copyrighted course materials, lecture content, or proprietary educational resources from any institution or instructor.

---

## The AMCD Framework

### The Problem AMCD Addresses

Technical education faces a fundamental tension: courses designed for beginners often bore advanced learners, while rigorous academic content alienates practical practitioners. Instructors frequently create entirely separate courses for different audiences, duplicating effort and fragmenting quality.

### The AMCD Solution

AMCD resolves this tension through a simple but powerful principle: **separate what must remain consistent from what should be customized**.

**CORE (Stable for All Learners)**
- **C**aptivate: Hook with story, establish relevance
- **O**rient: Build systematic understanding
- **R**ealize: Apply concepts through case study
- **E**xecute: Hands-on practice with guidance

**FLEX (Adapts to Audience)**
- **F**it to learner level
- **L**evel the options (2-3 tiers)
- **E**quivalent effort across tiers
- **X**pand to scale (module → pathway → course)

This separation enables instructors to maintain pedagogical integrity while serving diverse audiences efficiently.

---

## Who This Is For

| Audience | Primary Resources | Focus |
|----------|-------------------|-------|
| **Course designers and instructors** | AMCD methodology, CORE formula, templates | Designing better courses |
| **Institutions evaluating adoption** | Methodology paper, institutional guides | Due diligence and implementation planning |
| **Researchers and collaborators** | Full methodology paper, theoretical foundations | Understanding the framework's basis |

---

## Quick Start

### For Course Designers

1. **Read the CORE Formula**: [instruction-guides/individual-designers/the-core-formula.md](instruction-guides/individual-designers/the-core-formula.md)
2. **Review the template**: [templates/master-course-template.md](templates/master-course-template.md)
3. **Start designing**: Apply the 4-lesson structure to your first module

### For Institutions

1. **Executive Summary**: [instruction-guides/institutions/executive-summary.md](instruction-guides/institutions/executive-summary.md)
2. **Methodology Overview**: [instruction-guides/institutions/methodology-overview.md](instruction-guides/institutions/methodology-overview.md)
3. **Implementation Guide**: [instruction-guides/institutions/implementation-guide.md](instruction-guides/institutions/implementation-guide.md)

### For Deep Understanding

**Read the full methodology paper**: [papers/adaptive-modular-course-design.md](papers/adaptive-modular-course-design.md)

This paper presents the complete theoretical foundations, synthesizing 12 peer-reviewed educational theories into the AMCD framework.

---

## The CORE Formula

Every module uses exactly four lessons:

```
┌─────────────────────────────────────────────────────────────┐
│                     THE CORE FORMULA                         │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  C - CAPTIVATE  →  O - ORIENT  →  R - REALIZE  →  E - EXECUTE │
│                                                              │
│  "Why care?"      "How work?"    "When apply?"    "Do it!"   │
│                                                              │
│  Hook them        Teach them     Show them        Let them   │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

Each lesson type has a distinct teaching voice:

| Lesson | Voice | Energy | Purpose |
|--------|-------|--------|---------|
| Captivate | Enthusiastic Storyteller | 7/10 | Create engagement before education |
| Orient | Patient Systematizer | 5/10 | Build understanding step by step |
| Realize | Empathetic Navigator | 6/10 | Show concepts through human experience |
| Execute | Focused Coach | 4/10 | Direct, practical guidance |

This voice variation isn't arbitrary—it reflects how skilled educators naturally shift their approach based on instructional goals.

---

## Theoretical Foundations

AMCD synthesizes 12 established educational theories:

1. **Bloom's Revised Taxonomy** (Anderson & Krathwohl, 2001) — Learning objective structure
2. **Cognitive Load Theory** (Sweller, 1988) — Managing mental effort
3. **Zone of Proximal Development** (Vygotsky, 1978) — Appropriate challenge levels
4. **Scaffolding** (Bruner et al., 1976) — Structured support
5. **Differentiated Instruction** (Tomlinson, 1999) — Meeting learners where they are
6. **Narrative Pedagogy** (Bruner, 1986) — Story as learning structure
7. **Mastery Learning** (Bloom, 1968) — Competency demonstration
8. **Spiral Curriculum** (Bruner, 1960) — Progressive revisitation
9. **Backward Design** (Wiggins & McTighe, 2005) — Outcomes-first design
10. **Experiential Learning** (Kolb, 1984) — Learning through doing
11. **Constructivist Assessment** — Portfolio-based evaluation
12. **Project-Based Learning** — Authentic, extended tasks

The methodology paper provides detailed citations and explains how each theory informs specific framework components.

---

## The Role of the Agentic Course Creator (ACC)

The [Agentic Course Creator](agentic-course-creator/README.md) included in this repository is **not a finished product, automation tool, or implementation layer**.

It serves three purposes:

1. **Demonstration**: Illustrates how AMCD can be operationalized using AI agents
2. **Research Companion**: Explores how symbolic rubrics, instruction styles, and structured lesson archetypes interact with AI-assisted content creation
3. **Open-Core Reference**: Provides high-level guidance for future implementation and experimentation—not a turnkey system

**ACC should be viewed as a supporting asset, not the focal point.**

Its inclusion strengthens confidence in AMCD's applicability and future extensibility rather than serving as a standalone commercial or developer-ready tool.

---

## Repository Structure

```
agentic-professor/
├── README.md                           # This file
├── papers/
│   ├── adaptive-modular-course-design.md   # Full methodology paper (primary contribution)
│   ├── AMCD-one-pager.md               # Executive summary
│   └── AMCD-quick-guide.md             # Quick reference
├── templates/
│   └── master-course-template.md       # Comprehensive course template
├── instruction-guides/
│   ├── institutions/                   # For institutional decision-makers
│   └── individual-designers/           # For course creators
├── agentic-course-creator/             # Supporting demonstration asset
│   ├── agents/                         # Agent specifications (exploratory)
│   ├── guides/developers/              # Technical reference
│   └── workflows/                      # Process documentation
└── LICENSE
```

---

## Design Principles

### 1. Fundamentals First
Teach foundational concepts before advanced features. Strong foundations enable rapid learning.

### 2. Rationale-Driven
Every concept includes the "why" with tradeoffs. Students understand reasoning, not just mechanics.

### 3. Show-Then-Try
Brief demonstrations followed by immediate practice. Learning happens through doing.

### 4. Outcome-Focused
Every module produces a tangible, portfolio-ready artifact. Theory serves practice, not vice versa.

### 5. Progressive Complexity
Layer concepts from basic → typical → advanced. Build understanding incrementally.

---

## Getting Started: Three Approaches

### Approach 1: Human-Led Design
1. Read the [master template](templates/master-course-template.md)
2. Choose your subject area
3. Follow the CORE structure for each module
4. Use checklists to validate quality

**Time investment:** 8-12 hours per module

### Approach 2: AI-Assisted Design
1. Provide the template and methodology to an LLM
2. Specify subject, audience level, learning objectives
3. Review generated content against AMCD principles
4. Refine voice consistency and add expertise

**Time investment:** 3-5 hours per module

### Approach 3: Hybrid Approach (Recommended)
1. Use AI to generate first draft following AMCD structure
2. Revise hook and case study with personal experience
3. Validate technical accuracy
4. Customize for your specific context

**Time investment:** 4-6 hours per module

---

## Validation and Limitations

### What AMCD Provides

- A research-grounded structure for course design
- Repeatable patterns that address common instructional weaknesses
- Clear separation of stable content from audience-adaptable practice
- Voice variation that reflects effective teaching practice

### What AMCD Does Not Provide

- Empirical validation of learning outcomes (this requires further research)
- Automated course generation (the ACC is exploratory, not production-ready)
- Domain-specific content expertise (your subject matter knowledge is essential)
- Guarantee of results (no methodology can promise specific outcomes)

### Claims and Evidence

Throughout this repository, we distinguish between:
- **Design goals**: What the framework is intended to achieve
- **Theoretical support**: What established research suggests
- **Preliminary observations**: What initial application indicates
- **Validated outcomes**: What empirical testing has confirmed

Most claims in this repository fall into the first three categories. Rigorous validation requires further empirical study.

---

## Author

**Bradley Ross**
Harvard Educator | AI Systems Specialist

- **LinkedIn**: [linkedin.com/in/bradleyross](https://linkedin.com/in/bradleyross)

AMCD was developed from practical experience teaching AI engineering and technical courses at the university level, combined with systematic study of educational research.

---

## License

MIT License - see [LICENSE](LICENSE) file for details.

You are free to use, modify, and distribute this framework for educational purposes with attribution.

---

## Citation

If you use this framework in academic or professional work, please cite:

```
Ross, B. (2024). Adaptive Modular Course Design: A Framework for Scalable
Technical Education (Version 2.0.0). https://github.com/bar181/agentic-professor
```

---

## Acknowledgments

This framework synthesizes established educational methodologies into a practical course design structure. It draws from:

- Bloom's taxonomy and cognitive load research
- Constructivist and experiential learning theory
- Narrative pedagogy and storytelling research
- Differentiated instruction and scaffolding principles
- Project-based and mastery learning approaches

No copyrighted course materials, lecture content, or proprietary educational content from any institution or instructor are reproduced or included.

---

**Ready to design your first module?**

→ Start with [The CORE Formula](instruction-guides/individual-designers/the-core-formula.md)

→ Or read [the full methodology](papers/adaptive-modular-course-design.md)
