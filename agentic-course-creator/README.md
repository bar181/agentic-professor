# Agentic Course Creator

**An AI-Powered System for Generating Complete Courses Using the CORE + FLEX Framework**

**Version:** 1.0.0
**Framework:** Adaptive Modular Course Design (AMCD)
**Architecture:** Multi-Agent Orchestration with Specialized Content Agents

---

## Overview

The Agentic Course Creator is a comprehensive system that leverages AI agents to generate complete educational courses based on the CORE + FLEX framework. Course designers provide high-level requirements, and the system orchestrates specialized agents to produce fully-realized course content.

### What This System Does

1. **Accepts Designer Input**: Course topic, audience, objectives, difficulty level, length, and any source materials
2. **Researches & Plans**: Gathers domain knowledge, structures curriculum, designs learning arcs
3. **Generates Content**: Creates all four CORE lessons for each module using persona-driven templates
4. **Creates Problem Sets**: Produces tiered FLEX problem sets adapted to target audiences
5. **Assembles Pathways & Courses**: Structures modules into pathways with mini-capstones and courses with capstones
6. **Enables Rapid Iteration**: Supports quick editing, adaptation, and refinement

---

## The CORE + FLEX Framework (Review)

```
┌────────────────────────────────────────────────────────────────┐
│                    THE CORE + FLEX MODEL                        │
├────────────────────────────────────────────────────────────────┤
│         CORE (Stable)              +           FLEX (Adaptive) │
│                                                                 │
│   C - Captivate (Hook)                 F - Fit to learner       │
│   O - Orient (Understand)              L - Level the options    │
│   R - Realize (Apply)                  E - Equivalent effort    │
│   E - Execute (Practice)               X - eXpand to scale      │
│                                                                 │
│   = 4 Lessons                          = Tiered Problem Sets    │
└────────────────────────────────────────────────────────────────┘
```

---

## System Architecture

```
┌─────────────────────────────────────────────────────────────────────────┐
│                        COURSE DESIGNER INPUT                             │
│  (topic, audience, objectives, difficulty, length, source materials)    │
└────────────────────────────────────────┬────────────────────────────────┘
                                         │
                                         ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                         ORCHESTRATOR AGENT                               │
│  • Parses configuration                                                  │
│  • Coordinates all agents                                                │
│  • Manages workflow state                                                │
│  • Assembles final output                                                │
└───────┬─────────────┬─────────────┬─────────────┬─────────────┬────────┘
        │             │             │             │             │
        ▼             ▼             ▼             ▼             ▼
┌───────────┐ ┌───────────┐ ┌───────────┐ ┌───────────┐ ┌───────────┐
│ RESEARCH  │ │ STRUCTURE │ │  CONTENT  │ │  PROBLEM  │ │  QUALITY  │
│  AGENTS   │ │  AGENTS   │ │  AGENTS   │ │   SETS    │ │  AGENTS   │
├───────────┤ ├───────────┤ ├───────────┤ ├───────────┤ ├───────────┤
│• Topic    │ │• Module   │ │• Captivate│ │• Tier Gen │ │• Content  │
│  Research │ │  Architect│ │• Orient   │ │• Skill    │ │  Review   │
│• Example  │ │• Pathway  │ │• Realize  │ │  Adapter  │ │• Bloom's  │
│  Finder   │ │  Architect│ │• Execute  │ │• Role     │ │  Validate │
│• Source   │ │• Course   │ │           │ │  Adapter  │ │• Voice    │
│  Analyzer │ │  Architect│ │           │ │           │ │  Check    │
└───────────┘ └───────────┘ └───────────┘ └───────────┘ └───────────┘
        │             │             │             │             │
        └─────────────┴─────────────┴──────┬──────┴─────────────┘
                                           │
                                           ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                         ADAPTATION AGENTS                                │
│  • Workshop Adapter (half-day, full-day, multi-day)                     │
│  • Platform Adapter (Udemy, Coursera, University LMS)                   │
│  • Format Adapter (video scripts, interactive, text-based)              │
└────────────────────────────────────────┬────────────────────────────────┘
                                         │
                                         ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                          COMPLETE COURSE OUTPUT                          │
│  • Full course structure with all modules                               │
│  • All 4 CORE lessons per module                                        │
│  • Tiered FLEX problem sets                                             │
│  • Pathway mini-capstones                                               │
│  • Course capstone project                                              │
│  • Instructor guides and materials                                       │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## Directory Structure

```
agentic-course-creator/
├── README.md                          # This file
├── config/
│   ├── course-config-schema.json      # Input schema specification
│   ├── default-config.yaml            # Default parameters
│   └── examples/                      # Example configurations
│       ├── executive-workshop.yaml
│       ├── university-course.yaml
│       └── bootcamp-module.yaml
├── agents/
│   ├── orchestrator.md                # Main coordination agent
│   ├── content/                       # CORE lesson generators
│   │   ├── lesson-captivate.md        # Lesson 1: Hook
│   │   ├── lesson-orient.md           # Lesson 2: Understanding
│   │   ├── lesson-realize.md          # Lesson 3: Application
│   │   └── lesson-execute.md          # Lesson 4: Hands-On
│   ├── problem-sets/                  # FLEX generators
│   │   ├── tier-generator.md          # Creates tiered problems
│   │   ├── skill-level-adapter.md     # Adapts by skill
│   │   └── role-adapter.md            # Adapts by role
│   ├── structure/                     # Architecture agents
│   │   ├── module-architect.md
│   │   ├── pathway-architect.md
│   │   └── course-architect.md
│   ├── quality/                       # QA agents
│   │   ├── content-reviewer.md
│   │   ├── bloom-validator.md
│   │   └── voice-consistency.md
│   ├── research/                      # Knowledge gathering
│   │   ├── topic-researcher.md
│   │   └── example-finder.md
│   └── adaptation/                    # Format conversion
│       ├── workshop-adapter.md
│       └── platform-adapter.md
├── templates/                         # Output templates
│   ├── module/
│   ├── problem-sets/
│   ├── pathway/
│   ├── course/
│   └── workshop/
├── workflows/                         # End-to-end workflows
│   ├── full-course-workflow.md
│   ├── module-only-workflow.md
│   ├── enhancement-workflow.md
│   └── workshop-conversion.md
├── prompts/                           # Reusable prompts
│   ├── system-prompts/
│   └── task-prompts/
└── output/                            # Generated courses
```

---

## Quick Start

### 1. Define Your Course Configuration

Create a YAML configuration file (see `config/examples/`):

```yaml
course:
  title: "Introduction to AI Agents"
  topic: "Building AI agent systems with LLMs"
  description: "A comprehensive course on designing, building, and deploying AI agents"

audience:
  primary: "Software developers"
  level: "intermediate"
  prerequisites:
    - "Basic Python programming"
    - "Familiarity with APIs"

parameters:
  reading_level: "professional"
  difficulty: "intermediate"
  ai_content_ratio: 0.8  # 80% AI-generated, 20% designer input
  total_hours: 30

structure:
  pathways: 3
  modules_per_pathway: 4
  include_capstone: true
  include_mini_capstones: true

problem_sets:
  tiers:
    - name: "Foundation"
      target: "beginners building first agent"
    - name: "Standard"
      target: "developers building production agents"
    - name: "Advanced"
      target: "engineers optimizing complex systems"
  time_per_tier: 45  # minutes

delivery:
  format: "async_online"
  platform: "custom_lms"
  workshop_variant: true
```

### 2. Run the Orchestrator

```bash
# Using Claude or compatible AI system
./run-orchestrator.sh --config my-course.yaml --output ./output/my-course/
```

Or invoke directly:

```
Orchestrator Agent:
- Read configuration from: config/examples/my-course.yaml
- Execute full-course-workflow
- Output to: output/my-course/
```

### 3. Review and Refine

The system outputs complete course content that you can:
- Review and edit directly
- Run through QA agents for validation
- Adapt for different platforms or formats
- Iterate on specific modules

---

## Designer Input Parameters

### Required Inputs

| Parameter | Description | Example |
|-----------|-------------|---------|
| `title` | Course title | "AI Agent Fundamentals" |
| `topic` | Core subject matter | "Building autonomous AI systems" |
| `audience.primary` | Target learner | "Software engineers" |
| `audience.level` | Skill level | beginner/intermediate/advanced |
| `parameters.total_hours` | Course length | 20-60 hours |

### Optional Inputs

| Parameter | Description | Default |
|-----------|-------------|---------|
| `parameters.reading_level` | Content complexity | Matches audience.level |
| `parameters.ai_content_ratio` | AI vs designer content | 0.8 (80%) |
| `parameters.difficulty` | Problem set difficulty | Matches audience.level |
| `structure.pathways` | Number of pathways | 3 |
| `structure.modules_per_pathway` | Modules per pathway | 3-4 |
| `problem_sets.tiers` | Custom tier definitions | Less/Standard/More |
| `delivery.format` | Delivery mode | async_online |
| `delivery.workshop_variant` | Create workshop version | false |

### Source Materials (Optional)

Designers can provide:
- **Research papers**: Academic foundations for content
- **Existing courses**: Prior content to enhance/adapt
- **Industry examples**: Real-world case studies
- **Documentation**: Technical specifications to teach
- **Expert interviews**: SME knowledge to incorporate

---

## Agent Specifications

### Orchestrator Agent

**Purpose**: Coordinates all other agents, manages workflow, assembles output

**Key Responsibilities**:
1. Parse and validate course configuration
2. Sequence agent invocations
3. Manage state and dependencies
4. Handle errors and retries
5. Assemble final course package

### Content Agents (CORE)

| Agent | Lesson | Persona | Energy | Output |
|-------|--------|---------|--------|--------|
| Captivate | 1 | Malan-style | 7/10 | Hook, big picture, motivation |
| Orient | 2 | Ng-style | 5/10 | Technical depth, examples |
| Realize | 3 | Williams-style | 6/10 | Case study, real-world impact |
| Execute | 4 | Ross-style | 4/10 | Hands-on, demonstrations |

### Problem Set Agents (FLEX)

| Agent | Purpose | Output |
|-------|---------|--------|
| Tier Generator | Create multi-tier problems | Problems at each difficulty |
| Skill Adapter | Match to skill level | Scaffolding adjustments |
| Role Adapter | Match to job role | Context-specific problems |

### Quality Agents

| Agent | Purpose | Checks |
|-------|---------|--------|
| Content Reviewer | Quality validation | Clarity, accuracy, completeness |
| Bloom Validator | Taxonomy alignment | Cognitive level progression |
| Voice Consistency | Persona adherence | Tone, energy, style |

---

## Workflow Modes

### Full Course Creation

```
Input → Research → Structure → Content → Problem Sets → QA → Adaptation → Output
```

Creates complete course with all pathways, modules, lessons, and problem sets.

### Module Only

```
Input → Research → Module Content → Problem Sets → QA → Output
```

Creates a single module for rapid prototyping or course extension.

### Enhancement

```
Existing Course → Analysis → Gap Identification → Content Updates → QA → Output
```

Improves existing course content using AMCD principles.

### Workshop Conversion

```
Full Course → Workshop Adapter → Condensed Format → Output
```

Converts course modules to workshop format (half-day, full-day, multi-day).

---

## Quality Assurance

Every generated course passes through QA agents that verify:

### Content Quality
- [ ] Clear, accurate explanations
- [ ] Appropriate complexity for audience
- [ ] Engaging hooks and examples
- [ ] Error-free code samples

### AMCD Compliance
- [ ] Four lessons per module (CORE)
- [ ] Tiered problem sets (FLEX)
- [ ] Time equivalence across tiers
- [ ] Persona voice consistency

### Bloom's Alignment
- [ ] Lesson 1: Remember/Understand
- [ ] Lesson 2: Understand/Apply
- [ ] Lesson 3: Apply/Analyze
- [ ] Lesson 4: Evaluate/Create

### Portfolio Artifacts
- [ ] Clear deliverable per module
- [ ] Pathway mini-capstones defined
- [ ] Course capstone comprehensive

---

## Example Use Cases

### University Course (15 weeks)
- 3 pathways × 4 modules = 12 modules
- 48 lessons (12 × 4)
- 36-48 problem sets (3-4 tiers per module)
- 3 mini-capstones + 1 capstone
- ~45 hours student work

### Executive Workshop (1 day)
- 1 pathway × 2 modules = 2 modules
- 8 lessons condensed to 6 hours
- 2 problem sets (executive tier)
- 1 synthesis activity

### Bootcamp Sprint (2 weeks)
- 2 pathways × 3 modules = 6 modules
- 24 lessons
- 18 problem sets (3 tiers)
- 2 mini-capstones + 1 capstone
- ~60 hours intensive

---

## Integration Points

### AI Providers
- Claude (Anthropic) - Primary
- GPT-4 (OpenAI) - Supported
- Local LLMs - Possible with adapters

### Output Formats
- Markdown (default)
- HTML
- SCORM packages
- PDF
- Platform-specific (Udemy, Coursera, Canvas)

### Source Integrations
- Web search for examples
- Academic databases for research
- GitHub for code samples
- Documentation sites

---

## Customization

### Adding New Personas

1. Create persona definition in `prompts/system-prompts/`
2. Define voice characteristics, energy level, patterns
3. Add to content agent configuration
4. Update orchestrator to use new persona

### Custom Problem Set Tiers

1. Define tier in configuration
2. Specify target audience characteristics
3. Set scaffolding level
4. Configure time allocation

### Platform Adapters

1. Create adapter in `agents/adaptation/`
2. Define platform constraints (video length, quiz format)
3. Implement transformation rules
4. Add to workflow options

---

## Limitations and Considerations

### What Works Well
- Structured course content generation
- Consistent voice and tone
- Scalable content production
- Multi-tier problem set creation

### Requires Human Review
- Technical accuracy verification
- Industry-specific nuances
- Cultural context adaptation
- Edge case handling

### Not Suitable For
- Highly specialized domain content without SME input
- Courses requiring original research
- Real-time adaptive learning
- Certification-level assessment design

---

## Version History

**v1.0.0** - Initial release with full agent system

---

## License

MIT License - See LICENSE file

---

*Built on the AMCD framework for scalable, quality technical education.*
