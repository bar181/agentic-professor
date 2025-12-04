# Full Course Creation Workflow

**End-to-End Process for Creating Complete Courses with the Agentic Course Creator**

---

## Workflow Overview

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         FULL COURSE WORKFLOW                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐              │
│  │ 1. INPUT │ -> │ 2. PLAN  │ -> │ 3. BUILD │ -> │ 4. QA    │ -> OUTPUT    │
│  │          │    │          │    │          │    │          │              │
│  │ Config   │    │ Research │    │ Content  │    │ Review   │    Course    │
│  │ + Source │    │ + Design │    │ + Adapt  │    │ + Refine │    Package   │
│  └──────────┘    └──────────┘    └──────────┘    └──────────┘              │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Phase 1: Input & Configuration

### Step 1.1: Create Course Configuration

**Human Task**: Designer creates YAML configuration file

```yaml
# Minimum viable configuration
course:
  title: "Your Course Title"
  topic: "Core subject matter"

audience:
  primary: "Target learner"
  level: "beginner|intermediate|advanced"

parameters:
  total_hours: 30
```

**Validation**: Orchestrator validates against schema

### Step 1.2: Gather Source Materials (Optional)

**Human Task**: Provide any of:
- Research papers or articles
- Existing course content to enhance
- Documentation to teach
- Case study examples

**Agent Task**: Source Analyzer processes materials

### Step 1.3: Initialize Workflow State

**Orchestrator Task**: Create workflow state object

```json
{
  "workflow_id": "course-{uuid}",
  "status": "initialized",
  "config": { ... },
  "progress": {
    "phase": "input",
    "pathways_completed": 0,
    "modules_completed": 0
  },
  "outputs": {}
}
```

---

## Phase 2: Research & Planning

### Step 2.1: Topic Research

**Agent**: topic-researcher

**Input**: Course topic, domain, audience level

**Output**:
- Core concepts (hierarchy)
- Key vocabulary
- Common misconceptions
- Case study ideas
- Suggested structure

**Duration**: ~5 minutes

### Step 2.2: Example Gathering

**Agent**: example-finder (parallel with 2.1)

**Input**: Topic, domain, audience

**Output**:
- Real-world applications
- Code examples
- Case studies
- Industry references

**Duration**: ~3 minutes

### Step 2.3: Course Architecture

**Agent**: course-architect

**Input**: Config + research outputs

**Output**:
- Complete course structure
- Pathway definitions
- Module outlines
- Capstone design
- Time allocations

**Duration**: ~3 minutes

### Step 2.4: Pathway Design

**Agent**: pathway-architect (for each pathway)

**Input**: Course structure, pathway number

**Output**:
- Module sequence
- Learning objectives per module
- Mini-capstone design
- Dependencies

**Duration**: ~2 minutes per pathway

### Step 2.5: Module Planning

**Agent**: module-architect (for each module)

**Input**: Pathway structure, module number

**Output**:
- 3 learning objectives
- Portfolio artifact
- Key concepts
- Hero scenario
- Problem set context

**Duration**: ~1 minute per module

---

## Phase 3: Content Generation

### Step 3.1: Generate CORE Lessons

**For each module**, run in sequence:

#### Lesson 1: Captivate
**Agent**: lesson-captivate

**Input**: Module plan, hero, research

**Output**: 400-600 word hook lesson

**Duration**: ~2 minutes

#### Lesson 2: Orient
**Agent**: lesson-orient

**Input**: Module plan, Lesson 1 reference

**Output**: 600-800 word technical lesson

**Duration**: ~3 minutes

#### Lesson 3: Realize
**Agent**: lesson-realize

**Input**: Module plan, hero, Lessons 1-2

**Output**: 500-700 word case study

**Duration**: ~3 minutes

#### Lesson 4: Execute
**Agent**: lesson-execute

**Input**: Module plan, all prior lessons

**Output**: Activity with specifications

**Duration**: ~2 minutes

### Step 3.2: Generate Problem Sets

**Agent**: tier-generator

**Input**: Module content, tier configuration

**Output**: 2-4 tiered problem sets

**Duration**: ~3 minutes per module

### Step 3.3: Generate Capstones

**Agent**: capstone-generator

**Inputs**:
- Pathway content (for mini-capstones)
- All pathway content (for course capstone)

**Output**: Capstone project specifications

**Duration**: ~5 minutes

---

## Phase 4: Quality Assurance

### Step 4.1: Content Review

**Agent**: content-reviewer (for each lesson)

**Input**: Lesson content, context

**Output**:
- Score (0-100)
- Issues list
- Improvement suggestions

**Decision Logic**:
- Score ≥ 90: Approve
- Score 80-89: Minor revisions (auto-apply)
- Score 70-79: Revisions needed (regenerate section)
- Score < 70: Flag for human review

### Step 4.2: Bloom's Validation

**Agent**: bloom-validator (for each module)

**Input**: All 4 lessons

**Output**:
- Bloom's progression check
- Cognitive level alignment
- Improvement suggestions

### Step 4.3: Voice Consistency

**Agent**: voice-consistency (for each module)

**Input**: All 4 lessons

**Output**:
- Persona adherence scores
- Energy level checks
- Tone consistency

### Step 4.4: Revision Loop

**If revisions needed**:

```
While quality_score < threshold:
    1. Collect feedback from reviewers
    2. Re-invoke content agent with feedback
    3. Re-run quality check
    4. Max 3 iterations, then flag for human
```

---

## Phase 5: Adaptation (Optional)

### Step 5.1: Workshop Conversion

**If workshop_variant: true**

**Agent**: workshop-adapter

**Input**: Selected modules, workshop config

**Output**:
- Workshop schedule
- Facilitator guide
- Participant materials
- Activities

### Step 5.2: Platform Adaptation

**If platform != markdown**

**Agent**: platform-adapter

**Input**: All content, platform specs

**Output**:
- Platform-formatted content
- Import packages (if applicable)

---

## Phase 6: Assembly & Output

### Step 6.1: Compile Course Package

**Orchestrator Task**: Assemble all outputs

**Structure**:
```
output/{course-name}/
├── course-overview.md
├── instructor-guide.md
├── pathway-1/
│   ├── pathway-overview.md
│   ├── module-1/
│   │   ├── lesson-1-captivate.md
│   │   ├── lesson-2-orient.md
│   │   ├── lesson-3-realize.md
│   │   ├── lesson-4-execute.md
│   │   └── problem-sets/
│   │       ├── tier-1-foundation.md
│   │       ├── tier-2-standard.md
│   │       └── tier-3-advanced.md
│   ├── module-2/
│   ├── module-3/
│   ├── module-4/
│   └── mini-capstone.md
├── pathway-2/
├── pathway-3/
├── capstone/
│   └── capstone-project.md
├── workshop/  (if generated)
│   ├── facilitator-guide.md
│   └── participant-materials.md
└── metadata.yaml
```

### Step 6.2: Generate Metadata

**Orchestrator Task**: Create summary metadata

```yaml
metadata:
  generated_at: timestamp
  workflow_id: string
  quality_scores:
    average: number
    lowest: number
  statistics:
    total_words: number
    total_lessons: number
    total_problem_sets: number
  issues_flagged: list
  human_review_needed: boolean
```

### Step 6.3: Final Report

**Orchestrator Task**: Generate completion report

```markdown
# Course Generation Report

## Summary
- Course: {title}
- Generated: {timestamp}
- Duration: {minutes} minutes

## Statistics
- Pathways: 3
- Modules: 12
- Lessons: 48
- Problem Sets: 36
- Total Words: ~45,000

## Quality
- Average Score: 91/100
- Modules Needing Review: 0

## Ready for: [Human Review | Publication]
```

---

## Timing Estimates

### Total Generation Time by Course Size

| Course Size | Pathways | Modules | Estimated Time |
|-------------|----------|---------|----------------|
| Small | 1 | 3-4 | 20-30 minutes |
| Medium | 2 | 6-8 | 40-60 minutes |
| Standard | 3 | 9-12 | 60-90 minutes |
| Large | 4+ | 12+ | 90-120 minutes |

### Phase Breakdown (Standard 12-Module Course)

| Phase | Duration | Parallelization |
|-------|----------|-----------------|
| Input/Config | 5 min | Human |
| Research | 10 min | 2 agents parallel |
| Planning | 15 min | Sequential |
| Content (48 lessons) | 40 min | 4 lessons parallel |
| Problem Sets | 15 min | 3 modules parallel |
| QA | 10 min | All parallel |
| Assembly | 5 min | Sequential |
| **Total** | **~90 min** | |

---

## Error Handling

### Recoverable Errors

| Error | Detection | Recovery |
|-------|-----------|----------|
| Agent timeout | No response in 60s | Retry with backoff |
| Quality below threshold | Score < 70 | Regenerate with feedback |
| Missing dependency | Agent reports missing input | Generate prerequisite first |

### Non-Recoverable Errors

| Error | Detection | Action |
|-------|-----------|--------|
| Invalid config | Schema validation fails | Halt, report to user |
| Agent fails 3 times | Retry limit exceeded | Skip section, flag for human |
| Critical content error | QA flags as dangerous | Halt, require human review |

---

## Human Checkpoints

### Required Human Review

1. **Before Start**: Approve configuration
2. **After Planning**: Approve course structure
3. **After Generation**: Review flagged content
4. **Before Publish**: Final approval

### Optional Human Intervention

- Override quality thresholds
- Provide additional context mid-workflow
- Skip sections
- Adjust parameters dynamically

---

## Workflow Commands

### Start Full Course
```
orchestrator --config course.yaml --output ./output/
```

### Resume Interrupted Workflow
```
orchestrator --resume workflow-{uuid}
```

### Generate Single Module
```
orchestrator --config course.yaml --module 1.3 --output ./output/
```

### Regenerate with Feedback
```
orchestrator --resume workflow-{uuid} --regenerate lesson-2.1 --feedback "More examples needed"
```

---

*This workflow produces complete, high-quality courses in approximately 90 minutes for a standard 12-module course.*
