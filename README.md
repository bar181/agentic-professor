# agentic-professor
Gold-standard course design templates for AI-first education by Bradley.Academy. For course designers, instructional developers, and AI agents. Practical first; fundamentals before features; outcomes over theory. Structured agents and templates using Bloom’s taxonomy, voice-consistent lessons, and portfolio-ready deliverables.

# Agentic Professor

**Structured course design template for technical education**

Create computer science, AI, and software engineering courses with clear learning objectives, voice-consistent lessons, and portfolio-ready deliverables.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-2.0.0-green.svg)](CHANGELOG.md)

---

## What This Is

A production-ready course design template that provides:

- **4-lesson module structure** with clear pedagogical progression
- **Bloom's taxonomy learning objectives** for measurable outcomes
- **Voice-guided instruction patterns** for consistent teaching quality
- **Portfolio-focused deliverables** that students can showcase
- **Structured format** suitable for human educators and AI course generation

Built for universities, bootcamps, professional training programs, and AI-assisted course creation.

---

## Who This Is For

**Educators** creating technical courses (CS, AI, software engineering, data science)  
**Instructional Designers** needing structured templates with proven pedagogy  
**AI Systems** generating educational content with consistent quality  
**Training Programs** building professional development curricula  
**Bootcamps** designing outcome-focused technical education

---

## Quick Start

### 1. Review the Template

Read the [Master Course Design Template](templates/master-course-template.md) to understand the structure.

### 2. Key Components

Each module contains:

- **Module-level**: North Star statement, 3 learning objectives, introduction, outcomes
- **Lesson 1**: Introduction (big picture, analogies, engagement)
- **Lesson 2**: Understanding (technical depth, examples, concepts)
- **Lesson 3**: Application (case study, real-world impact)
- **Lesson 4**: Activity (hands-on deliverable, portfolio artifact)

### 3. Lesson Voice Framework

Each lesson uses a specific teaching voice:

| Lesson | Voice Style | Purpose | Characteristics |
|:-------|:------------|:--------|:----------------|
| 1 | David Malan (CS50) | Hook & Context | Storytelling, analogies, big picture |
| 2 | Andrew Ng | Technical Depth | Clear examples, systematic, concept-focused |
| 3 | Robin Williams | Real-World Impact | Case studies, human connection, "so what" |
| 4 | CS50 Problem Set | Hands-On Work | Specifications, structure, deliverables |

### 4. Create Your First Module

1. Choose your subject area (database design, API development, machine learning, etc.)
2. Define 3 learning objectives using Bloom's taxonomy
3. Write your North Star statement (one-sentence ultimate purpose)
4. Follow the template structure for each of the 4 lessons
5. Use the built-in checklists to validate quality

---

## Core Principles

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

## Template Structure

```
Module Structure
├── North Star (one-sentence purpose)
├── Learning Objectives (3, following Bloom's taxonomy)
├── Module Introduction (200-400 words)
│
├── Lesson 1: Introduction - The Hook
│   ├── Opening with compelling scenario
│   ├── Big picture mental model
│   ├── Core concepts in plain English
│   └── Learning journey preview
│
├── Lesson 2: Understanding - The Deep Dive
│   ├── Technical concept breakdown
│   ├── Progressive examples (basic → complex)
│   ├── Pseudocode with explanations
│   └── Common patterns and variations
│
├── Lesson 3: Application - The Case Study
│   ├── Hero character with challenge
│   ├── Problem analysis (what went wrong)
│   ├── Solution journey (thinking process)
│   └── Impact and takeaway
│
├── Lesson 4: Activity - The Deliverable
│   ├── Clear specifications
│   ├── Getting started guidance
│   ├── Evaluation criteria
│   └── Optional extensions
│
└── Module Summary (mastery criteria)
```

---

## Example Learning Objectives

Following Bloom's taxonomy progression:

**Database Design Module:**
1. **Explain** the role of normalization in database efficiency (Understand)
2. **Design** a normalized schema for an e-commerce application (Apply)
3. **Evaluate** database performance and recommend optimizations (Evaluate)

**API Development Module:**
1. **Describe** RESTful design principles and their constraints (Understand)
2. **Implement** a REST API with proper resource modeling (Apply)
3. **Assess** API design tradeoffs and select appropriate patterns (Evaluate)

**Prompt Engineering Module:**
1. **Summarize** how prompt structure affects AI output quality (Understand)
2. **Create** contractual prompts with role, goal, and constraints (Apply)
3. **Critique** prompt effectiveness and iterate systematically (Evaluate)

---

## Template Features

### Built-In Quality Standards

- **Word count guidelines** for each section
- **Quality checklists** for self-validation
- **Anti-patterns** explicitly called out
- **Voice consistency** guidelines per lesson
- **Assessment rubrics** for student deliverables

### Pedagogical Rigor

- **Bloom's taxonomy** framework for learning objectives
- **Progressive disclosure** of complex concepts
- **Cognitive load** management through structure
- **Active learning** emphasis (show-then-try)
- **Metacognition** through reflection prompts

### Practical Focus

- **Portfolio artifacts** as primary outcomes
- **Real-world case studies** in every module
- **Code examples** with explanations
- **Getting started** guidance for activities
- **Extension challenges** for advanced learners

---

## Use Cases

### University Courses
Structure semester-long courses with consistent quality across modules. Each module = 1 week of instruction.

### Bootcamps
Create intensive training programs with portfolio-focused outcomes. Clear specifications support rapid learning.

### Professional Training
Design corporate upskilling programs with measurable learning objectives and practical deliverables.

### AI Course Generation
Provide structured format for LLMs to generate educational content. Template reduces ambiguity and ensures consistency.

### Self-Paced Learning
Create asynchronous courses where learners progress independently. Clear structure supports autonomous learning.

---

## Design Philosophy

This template is based on:

- **Outcome-focused methodology**: Learning demonstrates capability, not just knowledge
- **Manager-Intern model**: Learner controls scope/quality, tools/AI support execution
- **Iterative clarity**: Complexity builds through progressive refinement
- **Contractual instruction**: Clear specifications reduce ambiguity
- **Evidence-based pedagogy**: Grounded in learning science research

Created by Bradley, teaching fellow at Harvard CS50 and instructor of AI engineering courses.

---

## Repository Contents (v2.0.0)

```
agentic-professor/
├── README.md (this file)
├── LICENSE
├── templates/
│   └── master-course-template.md (comprehensive template)
└── CHANGELOG.md
```

**Coming Soon:**
- `/examples` - Complete course modules (database design, prompt engineering, web APIs)
- `/personas` - Detailed teaching voice profiles
- `/agents` - AI specifications for automated course generation
- `/tools` - Validation scripts and utilities

---

## Getting Started: Three Approaches

### Approach 1: Human-Led Design (Traditional)
1. Read the [master template](templates/master-course-template.md)
2. Choose your subject area
3. Fill in sections following the structure
4. Use checklists to validate quality
5. Iterate based on student feedback

**Time investment:** 8-12 hours per module

### Approach 2: AI-Assisted Design (Collaborative)
1. Provide the template to Claude/GPT-4
2. Specify: subject, audience level, learning objectives
3. Review generated content against checklists
4. Refine voice consistency and examples
5. Add subject-specific expertise

**Time investment:** 3-5 hours per module

### Approach 3: Hybrid Approach (Recommended)
1. Use AI to generate first draft from template
2. Revise introduction and case study with personal experience
3. Validate technical accuracy in Lesson 2
4. Customize activity specifications for your context
5. Test with real students and iterate

**Time investment:** 4-6 hours per module

---

## Template Quality Standards

### Module-Level Validation

- [ ] North Star statement is specific and outcome-focused
- [ ] Three learning objectives follow Bloom's taxonomy
- [ ] Module introduction is 200-400 words with clear hook
- [ ] Portfolio artifact is clearly defined

### Lesson-Level Validation

- [ ] Lesson 1: Engaging hook, analogies, big picture established
- [ ] Lesson 2: Concepts defined clearly, examples progress basic→complex
- [ ] Lesson 3: Case study includes problem, analysis, solution, impact
- [ ] Lesson 4: Clear specifications, evaluation criteria, getting-started guidance

### Voice Consistency

- [ ] Each lesson matches designated teaching voice
- [ ] Energy levels appropriate to content density
- [ ] Technical terms defined on first use
- [ ] Active voice used throughout

---

## Frequently Asked Questions

### Can I adapt this for non-technical subjects?

Yes. The structure works for any subject with clear learning objectives. The voice personas and examples may need adjustment for non-technical domains.

### How does this differ from traditional course design?

This template emphasizes portfolio artifacts over knowledge retention, uses voice-specific instruction patterns, and is structured for both human and AI use.

### Is this suitable for live teaching or just asynchronous?

Both. The template works for self-paced online courses and can be adapted for live lectures by using the lesson content as lecture notes.

### Can AI generate courses using this template?

Yes. The structured format with clear specifications reduces ambiguity in AI-generated content. Provide the template as context to Claude/GPT-4.

### What's the recommended module length?

Each module = approximately 4-6 hours of student work (reading, activities, reflection). A typical course has 8-12 modules.

### How do I assess student work?

Lesson 4 includes evaluation criteria for each deliverable. Use the provided checklists as assessment rubrics.

---

## Contributing

This is v2.0.0 - the initial release with core template. Future versions will include:

- Complete course examples
- Teaching voice persona specifications
- AI agent specifications for course generation
- Validation tools and scripts
- Community-contributed extensions

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on submitting improvements, examples, or new personas.

---

## License

MIT License - see [LICENSE](LICENSE) file for details.

You are free to use, modify, and distribute this template for educational purposes with attribution.

---

## Support & Community

- **Issues**: Report template problems or request features via GitHub Issues
- **Discussions**: Share course implementations and ask questions in GitHub Discussions
- **Website**: Documentation and examples at [planned]

---

## Version History

**v2.0.0** (Current) - Initial public release with comprehensive course design template  
See [CHANGELOG.md](CHANGELOG.md) for detailed version history.

---

## Citation

If you use this template in academic work, please cite:

```
Bradley. (2025). Agentic Professor: Structured Course Design Template 
for Technical Education (Version 2.0.0) [Computer software]. 
[https://github.com/bar181/agentic-professor](https://github.com/bar181/agentic-professor/)
```

---

## Acknowledgments

Template design based on:
- Harvard CS50 pedagogical approaches (David Malan)
- Stanford AI course methodology (Andrew Ng)
- Bloom's taxonomy framework for learning objectives
- Cognitive load theory and progressive disclosure research
- Outcome-focused instructional design principles

Built for the AI-first education era where human expertise and AI capabilities collaborate to create effective learning experiences.

---

**Ready to create your first module?** → [View the Master Template](templates/master-course-template.md)
