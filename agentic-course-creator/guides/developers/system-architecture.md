# System Architecture Guide

**Understanding How the Agentic Course Creator Works**

---

## Overview

The Agentic Course Creator (ACC) is a multi-agent system where specialized AI agents collaborate to generate complete educational courses. Each agent has a specific role, personality, and quality standards.

```
┌─────────────────────────────────────────────────────────────────────────┐
│                           ORCHESTRATOR                                   │
│                    (Coordinates all agents)                              │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐    │
│  │  RESEARCH   │  │  STRUCTURE  │  │   CONTENT   │  │   QUALITY   │    │
│  │   AGENTS    │  │   AGENTS    │  │   AGENTS    │  │   AGENTS    │    │
│  ├─────────────┤  ├─────────────┤  ├─────────────┤  ├─────────────┤    │
│  │ • Topic     │  │ • Course    │  │ • Captivate │  │ • Content   │    │
│  │   Researcher│  │   Architect │  │ • Orient    │  │   Reviewer  │    │
│  │ • Example   │  │ • Pathway   │  │ • Realize   │  │ • Bloom     │    │
│  │   Finder    │  │   Architect │  │ • Execute   │  │   Validator │    │
│  │             │  │ • Module    │  │ • Tier Gen  │  │ • Assessor  │    │
│  │             │  │   Planner   │  │             │  │             │    │
│  └─────────────┘  └─────────────┘  └─────────────┘  └─────────────┘    │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## Agent Categories

### 1. Research Agents

**Purpose**: Gather domain knowledge before content generation.

| Agent | Function | Output |
|-------|----------|--------|
| topic-researcher | Analyze topic domain | Core concepts, vocabulary, structure suggestions |
| example-finder | Locate real-world applications | Code examples, case studies, industry references |

**When They Run**: Phase 2 (Research & Planning)

**Key Interaction**: Outputs feed into Structure Agents.

### 2. Structure Agents

**Purpose**: Design course architecture and flow.

| Agent | Function | Output |
|-------|----------|--------|
| course-architect | Design overall course structure | Pathways, modules, capstone design |
| pathway-architect | Plan individual pathways | Module sequence, dependencies, mini-capstone |
| module-planner | Detail module components | Learning objectives, hero scenario, artifact |

**When They Run**: Phase 2 (Research & Planning)

**Key Interaction**: Receive research outputs, generate structure for Content Agents.

### 3. Content Agents

**Purpose**: Generate actual lesson and problem set content.

| Agent | Function | Lesson Type |
|-------|----------|-------------|
| lesson-captivate | Hook learners with story/relevance | Lesson 1 (CORE) |
| lesson-orient | Explain concepts systematically | Lesson 2 (CORE) |
| lesson-realize | Apply through case study | Lesson 3 (CORE) |
| lesson-execute | Guide hands-on activity | Lesson 4 (CORE) |
| tier-generator | Create tiered problem sets | FLEX component |

**When They Run**: Phase 3 (Content Generation)

**Key Interaction**: Sequential within module (L1 → L2 → L3 → L4), parallel across modules.

### 4. Quality Agents

**Purpose**: Review and validate generated content.

| Agent | Function | Output |
|-------|----------|--------|
| content-reviewer | Assess content quality | Score, issues, suggestions |
| bloom-validator | Check cognitive progression | Bloom's alignment report |
| course-assessor | Generate institutional scorecard | Compliance scorecard |

**When They Run**: Phase 4 (Quality Assurance)

**Key Interaction**: Can trigger regeneration if score below threshold.

### 5. Adaptation Agents

**Purpose**: Convert content for different formats/audiences.

| Agent | Function | Output |
|-------|----------|--------|
| workshop-adapter | Convert to workshop format | Facilitator guide, participant materials |
| platform-adapter | Export to LMS formats | SCORM, xAPI, platform-specific packages |
| audience-adapter | Adjust for different skill levels | Beginner/Advanced variants |

**When They Run**: Phase 5 (Adaptation) - Optional

---

## Data Flow

### Complete Workflow

```
INPUT                 PROCESS                           OUTPUT
─────                 ───────                           ──────

course.yaml  ──┬──>  [topic-researcher]  ───────────────────┐
               │     [example-finder]                        │
               │           │                                 │
               │           v                                 │
               └──>  [course-architect]  ──────────────────┐│
                           │                               ││
                           v                               ││
                     [pathway-architect] (per pathway)     ││
                           │                               ││
                           v                               ││
                     [module-planner] (per module)         ││
                           │                               ││
                           v                               ││
               ┌──> [lesson-captivate] ─────┐              ││
               │    [lesson-orient]    ─────┤              ││
               │    [lesson-realize]   ─────┤  per module  ││
               └──> [lesson-execute]   ─────┤              ││
                    [tier-generator]   ─────┘              ││
                           │                               ││
                           v                               ││
                     [content-reviewer]  ──────────────────┤│
                     [bloom-validator]                     ││
                           │                               ││
                           v                               ││
                     [course-assessor]  ───────────────────┤│
                           │                               vv
                           └──────────────────────>  course-package/
                                                          │
                                                          ├── overview.md
                                                          ├── pathway-1/
                                                          │   ├── module-1/
                                                          │   │   ├── lessons/
                                                          │   │   └── problem-sets/
                                                          │   └── ...
                                                          └── scorecard.yaml
```

### Inter-Agent Communication

Agents communicate through structured outputs:

```yaml
# Example: course-architect output
course_structure:
  title: "Message Queue Architecture"
  pathways:
    - name: "Foundations"
      modules:
        - id: "1.1"
          title: "Producer-Consumer Basics"
          objectives: [...]
          hero_context: "Dev, a backend engineer..."
```

Each agent's output schema is defined in its specification file.

---

## State Management

### Workflow State Object

```json
{
  "workflow_id": "course-abc123",
  "status": "content_generation",
  "config": { /* original config */ },
  "progress": {
    "phase": "content",
    "pathways_completed": 1,
    "modules_completed": 4,
    "current_module": "2.1"
  },
  "outputs": {
    "research": { /* research agent outputs */ },
    "structure": { /* structure agent outputs */ },
    "content": {
      "pathway-1": {
        "module-1": {
          "lessons": { /* generated lessons */ },
          "problem_sets": { /* generated problems */ },
          "quality_score": 92
        }
      }
    }
  },
  "issues": []
}
```

### Checkpointing

Workflow state is saved after each phase:
- Allows resume after interruption
- Enables targeted regeneration
- Supports incremental review

---

## Error Handling

### Retry Logic

```
Agent Call
    │
    v
┌─────────────┐
│ Success?    │──Yes──> Continue
└─────────────┘
    │ No
    v
┌─────────────┐
│ Retry < 3?  │──No───> Flag for Human Review
└─────────────┘
    │ Yes
    v
Wait (exponential backoff: 2s, 4s, 8s)
    │
    v
Retry Agent Call
```

### Quality Threshold Handling

```
Quality Score
    │
    v
┌─────────────┐
│ Score ≥ 90  │──Yes──> Approve
└─────────────┘
    │ No
    v
┌─────────────┐
│ Score ≥ 80  │──Yes──> Minor Revisions (auto)
└─────────────┘
    │ No
    v
┌─────────────┐
│ Score ≥ 70  │──Yes──> Regenerate with Feedback
└─────────────┘
    │ No
    v
Flag for Human Review
```

---

## Parallelization Strategy

### What Can Run in Parallel

| Level | Parallel Candidates |
|-------|-------------------|
| Research | topic-researcher + example-finder |
| Pathways | All pathways can generate simultaneously |
| Modules | Modules within a pathway (if no dependencies) |
| Quality | All review agents |

### What Must Be Sequential

| Dependency | Reason |
|------------|--------|
| Lesson 1 → 2 → 3 → 4 | Each builds on previous |
| Research → Structure | Structure needs research context |
| Content → QA | Can't review what doesn't exist |

---

## Extension Points

### Adding New Agent Types

1. Create agent specification (see [adding-agents.md](adding-agents.md))
2. Register with orchestrator
3. Define input/output schemas
4. Add to workflow at appropriate phase

### Custom Quality Rules

1. Modify scoring rubric in agent spec
2. Adjust thresholds as needed
3. Add new positive/negative behaviors

### Platform Integration

1. Create adaptation agent for target platform
2. Define export format mapping
3. Add to Phase 5 workflow

---

## Performance Characteristics

### Typical Generation Times

| Course Size | Modules | Approximate Time |
|-------------|---------|-----------------|
| Small | 3-4 | 20-30 minutes |
| Medium | 6-8 | 40-60 minutes |
| Standard | 9-12 | 60-90 minutes |
| Large | 12+ | 90-120 minutes |

### Cost Factors

- Each agent call consumes tokens
- Quality regeneration loops add cost
- Parallel execution reduces wall-clock time but not cost

---

## Best Practices

### For Modifying Agents

1. **Test incrementally**: Change one thing, generate, review
2. **Preserve soul/north star**: The core purpose should rarely change
3. **Score before deploying**: Generate sample content, calculate scores
4. **Document changes**: Note what you modified and why

### For Extending the System

1. **Follow the format**: Use Agent Format v2.0 structure
2. **Define clear boundaries**: Each agent should have one job
3. **Specify schemas**: Input and output formats must be explicit
4. **Add error handling**: Assume things will fail

---

*This architecture enables consistent, high-quality course generation while remaining flexible enough for customization and extension.*
