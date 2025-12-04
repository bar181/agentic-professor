# Implementation Guide

**Adopting AMCD and ACC in Your Institution**

---

## Implementation Overview

```
Phase 1          Phase 2          Phase 3          Phase 4
PREPARE          PILOT            SCALE            OPTIMIZE
────────         ─────            ─────            ────────
2-4 weeks        4-8 weeks        8-16 weeks       Ongoing

• Assess fit     • Single course  • Expand scope   • Measure results
• Build team     • Track metrics  • Train teams    • Refine process
• Configure      • Evaluate       • Integrate      • Share learnings
```

---

## Phase 1: Preparation (2-4 weeks)

### Step 1.1: Readiness Assessment

**Evaluate your institution against key success factors:**

| Factor | Assessment Questions | Ready? |
|--------|---------------------|--------|
| Subject matter expertise | Do you have SMEs who can validate content? | ☐ |
| Instructional design capacity | Can someone evaluate pedagogical quality? | ☐ |
| Technical infrastructure | Do you have LMS and content delivery? | ☐ |
| Process flexibility | Can you adopt new workflows? | ☐ |
| Leadership support | Is there backing for AI-assisted development? | ☐ |

**Minimum requirements:** 4/5 factors should be ready.

### Step 1.2: Team Assembly

**Core team for pilot:**

| Role | Responsibility | Time Commitment |
|------|---------------|-----------------|
| Project Lead | Coordination, decisions | 5-10 hrs/week |
| Subject Matter Expert | Content validation | 10-15 hrs/week |
| Instructional Designer | Pedagogical review | 10-15 hrs/week |
| Technical Lead | System setup, integration | 5-8 hrs (setup) |

**Optional:**
- Quality Assurance reviewer
- LMS administrator
- Faculty liaison

### Step 1.3: System Configuration

**Basic setup:**

1. **Configure core parameters**
   - Review default personality settings
   - Adjust energy levels and formality to match institutional voice
   - Customize scoring thresholds if needed

2. **Prepare input templates**
   - Course configuration YAML structure
   - Source material formatting guidelines
   - Learning objective templates

3. **Establish review workflow**
   - Who approves at each checkpoint?
   - What quality score triggers manual review?
   - How are revisions tracked?

### Step 1.4: Select Pilot Course

**Ideal pilot characteristics:**

| Characteristic | Why It Matters |
|---------------|----------------|
| Medium complexity | Not too simple, not too specialized |
| Willing SME | Engaged expert who will provide feedback |
| 4-6 modules | Enough to evaluate, not overwhelming |
| New or revision | Either works; new may be cleaner |
| Non-critical timeline | Room for learning without pressure |

**Avoid for pilot:**
- Highly regulated content requiring compliance review
- Cutting-edge topics with limited source material
- Courses with immovable deadlines
- Topics where accuracy is critical and hard to verify

---

## Phase 2: Pilot (4-8 weeks)

### Week 1-2: First Module

**Goals:**
- Generate first complete module
- Establish review rhythm
- Document friction points

**Process:**

```
Day 1-2: Generate CORE lessons
         ↓
Day 3-4: SME content review
         ↓
Day 5-6: ID pedagogical review
         ↓
Day 7-8: Revisions and finalization
         ↓
Day 9-10: Generate and review FLEX problem sets
```

**Track:**
- Time spent on each step
- Quality scores from system
- Number of revisions required
- Team feedback

### Week 3-4: Second and Third Modules

**Goals:**
- Improve efficiency
- Identify patterns in issues
- Refine review process

**Adjustments to make:**
- Common issues → Add to scoring rubric
- Slow steps → Streamline process
- Quality gaps → Increase review focus

### Week 5-6: Remaining Modules

**Goals:**
- Complete pilot course
- Achieve steady-state efficiency
- Prepare evaluation data

### Week 7-8: Evaluation

**Metrics to assess:**

| Metric | Target | Your Result |
|--------|--------|-------------|
| Total development time | 40-50% reduction | _____ |
| Quality score average | 85+ | _____ |
| Modules requiring major rework | <20% | _____ |
| Team satisfaction | Positive | _____ |
| SME satisfaction | Positive | _____ |

**Decision criteria:**

| Score | Recommendation |
|-------|----------------|
| 4-5 metrics met | Proceed to scale |
| 2-3 metrics met | Refine and repeat pilot |
| 0-1 metrics met | Reassess fit |

---

## Phase 3: Scale (8-16 weeks)

### Expand Scope Gradually

**Recommended progression:**

| Stage | Scope | Duration |
|-------|-------|----------|
| Stage 1 | 2-3 additional courses, same team | 4-6 weeks |
| Stage 2 | Department-wide, trained teams | 6-8 weeks |
| Stage 3 | Institution-wide, established process | Ongoing |

### Train Additional Teams

**Training curriculum:**

| Session | Duration | Content |
|---------|----------|---------|
| AMCD Overview | 2 hours | Framework, CORE+FLEX, quality standards |
| System Walkthrough | 2 hours | Configuration, generation, review |
| Hands-On Practice | 4 hours | Generate and review one module |
| Q&A and Troubleshooting | 1 hour | Address questions from practice |

**Training materials:**
- This implementation guide
- Methodology overview
- Sample configurations
- Example outputs

### Integrate with Existing Processes

**Integration points:**

| Process | Integration Approach |
|---------|---------------------|
| Curriculum approval | Add ACC output review to existing workflow |
| Quality assurance | Map ACC scoring to institutional QA |
| LMS publishing | Establish export/import procedures |
| Course maintenance | Define update triggers and process |

### Establish Governance

**Decision rights:**

| Decision | Who Decides |
|----------|-------------|
| Configuration changes | ID lead + technical lead |
| Quality threshold adjustments | QA + department head |
| New course adoption | Department + project lead |
| System modifications | Technical lead + governance |

---

## Phase 4: Optimize (Ongoing)

### Measure Continuously

**Key metrics dashboard:**

| Metric | Frequency | Target |
|--------|-----------|--------|
| Development time per module | Per project | Baseline -50% |
| Quality score average | Monthly | 88+ |
| Regeneration rate | Weekly | <15% |
| Team satisfaction | Quarterly | >4/5 |
| Learner outcomes | Per course | Baseline or better |

### Refine Based on Data

**Common optimizations:**

| Issue | Solution |
|-------|----------|
| Specific error type recurring | Add to scoring rubric with higher penalty |
| Review taking too long | Streamline checkpoints, pre-approve low-risk content |
| Voice not matching brand | Adjust personality configuration |
| Quality inconsistent by domain | Create domain-specific configurations |

### Share Learnings

**Build institutional knowledge:**
- Document successful patterns
- Create domain-specific configuration templates
- Develop FAQ from common questions
- Train champions in each department

---

## Common Implementation Challenges

### Challenge 1: Resistance from Faculty

**Signs:**
- Low engagement in review
- Criticism of AI involvement
- Requests to "do it the old way"

**Solutions:**
- Share time savings data
- Emphasize expert control over final output
- Position as draft tool, not replacement
- Find faculty champions for peer influence

### Challenge 2: Quality Issues in Specific Domains

**Signs:**
- Higher regeneration rates for certain topics
- More SME corrections needed
- Quality scores consistently lower

**Solutions:**
- Create domain-specific scoring rules
- Provide more source material to system
- Accept that some domains need more review
- Consider whether ACC is right fit for domain

### Challenge 3: Process Adoption

**Signs:**
- Teams skipping review steps
- Inconsistent quality across teams
- Workarounds developing

**Solutions:**
- Simplify workflow where possible
- Automate quality checkpoints
- Regular training refreshers
- Clear accountability for process adherence

### Challenge 4: Integration Difficulties

**Signs:**
- Manual steps between systems
- Format conversion problems
- Tracking gaps

**Solutions:**
- Invest in technical integration
- Standardize export formats
- Build automation scripts
- Accept some manual steps initially

---

## Success Factors Summary

### What Makes Implementation Successful

| Factor | Importance | Actions |
|--------|-----------|---------|
| Executive sponsorship | High | Secure visible support, remove obstacles |
| SME engagement | Critical | Choose willing participants, respect their time |
| Clear expectations | High | Communicate that review is required |
| Appropriate pilot | High | Not too complex, not too simple |
| Patience with learning curve | Medium | First projects take longer |
| Metrics discipline | Medium | Track and share results |

### Warning Signs to Watch

| Sign | Response |
|------|----------|
| No one reviewing output | Halt; review is not optional |
| Quality declining | Increase review rigor |
| Team frustration | Simplify process, get feedback |
| Stakeholder complaints | Address concerns, adjust expectations |
| No time savings | Analyze workflow, identify bottlenecks |

---

## Timeline Summary

| Phase | Duration | Key Milestones |
|-------|----------|----------------|
| Prepare | 2-4 weeks | Team formed, system configured, pilot selected |
| Pilot | 4-8 weeks | First course complete, metrics evaluated |
| Scale | 8-16 weeks | Multiple teams trained, process integrated |
| Optimize | Ongoing | Continuous improvement, knowledge sharing |

**Total time to initial value:** 6-12 weeks
**Total time to scaled adoption:** 6-9 months

---

## Getting Support

For implementation questions and consultation:

**Bradley Ross**
- Harvard educator, AI systems specialist
- Can provide guidance on fit assessment, configuration, and optimization
- LinkedIn: [linkedin.com/in/bradleyross](https://linkedin.com/in/bradleyross)

---

*Successful implementation requires patience, measurement, and willingness to adapt. Start small, learn fast, and scale what works.*
