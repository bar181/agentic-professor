# Master Course Design Template
## Universal Template for CS, Tech, AI, and Agentics Courses

**Version:** 2.0  
**Target Audience:** Course designers, instructional developers, AI agents creating educational content  
**Philosophy:** Practical first. Fundamentals before features. Outcomes over theory.

---

## Template Philosophy & North Star

Every module exists to transform a learner from **"I don't know how"** to **"I can build this and explain why it works."**

### Core Principles
1. **Fundamentals First** - Strong foundations before advanced features
2. **Rationale-Driven** - Every concept includes the "why" with tradeoffs
3. **Show-Then-Try** - Brief demonstrations followed by immediate practice
4. **Outcome-Focused** - Every module produces a tangible, portfolio-ready artifact
5. **Learner as Manager** - Students control scope and quality; tools/AI support execution

---

## Module-Level Structure

### 1. Module Metadata

```markdown
## Module [Number]: [Clear, Action-Oriented Title]

**Estimated Time:** [X] hours
**Prerequisites:** [List or "None"]
**Deliverable:** [One-sentence description of portfolio artifact]
```

### 2. North Star Statement

**Format:** One powerful sentence that captures the module's ultimate purpose.

**Template:**  
"By the end of this module, you will [specific capability] that enables you to [real-world outcome]."

**Examples:**
- "By the end of this module, you will design database schemas that scale to millions of users without breaking."
- "By the end of this module, you will architect prompts that produce consistent, predictable AI outputs."
- "By the end of this module, you will debug distributed systems using systematic failure analysis."

**Anti-patterns to avoid:**
- ❌ "Learn about databases"
- ❌ "Understand AI prompting"
- ❌ "Explore debugging techniques"

### 3. Learning Objectives (Exactly 3)

**Framework:** Use Bloom's Taxonomy progression
- Objective 1: **Remember/Understand** (foundational knowledge)
- Objective 2: **Apply/Analyze** (practical application)
- Objective 3: **Evaluate/Create** (mastery demonstration)

**Format:**  
Students will be able to [action verb] [specific skill] [context/constraint].

**Example Set:**
1. **Explain** the role of database indexes **in query optimization** (Understand)
2. **Design** normalized database schemas **for e-commerce applications** (Apply)
3. **Evaluate** database performance **using query analysis tools and recommend optimizations** (Evaluate)

**Verb Bank by Level:**
- Understand: explain, describe, summarize, interpret
- Apply: implement, demonstrate, use, execute
- Analyze: compare, contrast, differentiate, examine
- Evaluate: assess, critique, judge, recommend
- Create: design, build, architect, compose

### 4. Module Introduction (200-400 words)

**Purpose:** Hook the learner and establish relevance

**Voice:** Practical Expert meets Engaging Storyteller  
**Tone:** Confident, clear, minimal jargon, real-world grounded

#### Structure Template

**Paragraph 1 - The Hook (50-80 words)**
Start with a relatable frustration or compelling scenario from real development work.

> "You've just deployed your app. Five minutes later, it crashes. Users are locked out. Your database is timing out on queries that worked perfectly in testing. Sound familiar? This isn't a failure of code—it's a failure of database design."

**Paragraph 2 - The Relief (60-100 words)**
Introduce the core concept that solves the problem. Explain **why** this foundation matters.

> "Database design isn't just about storing data—it's about structuring information so your system can find, update, and scale efficiently. The difference between a slow app and a fast one often comes down to three decisions made before you wrote a single query. This module teaches you those three decisions."

**Paragraph 3 - The Promise (60-100 words)**
What will they build? What will they be able to do?

> "You'll learn to design schemas that handle real-world complexity, write queries that execute in milliseconds instead of seconds, and diagnose performance issues before they become production fires. By the end, you'll have designed and validated a database for [specific use case] that you can confidently explain to any technical team."

**Paragraph 4 - The Approach (40-80 words)**
How will this module teach differently?

> "We'll start with fundamentals—what makes a good schema—then layer on optimization techniques through a real case study with Alex, a developer building a social platform. You'll see the mistakes, the fixes, and most importantly, the reasoning behind every decision."

#### Quality Checklist
- [ ] Opens with concrete frustration or scenario (not theory)
- [ ] Defines one core concept in plain English within first 150 words
- [ ] Includes one analogy or metaphor
- [ ] Promises specific, portfolio-ready outcome
- [ ] Word count: 200-400 words
- [ ] Jargon ratio: <15% (define technical terms on first use)

### 5. Module Summary/Outcomes

**Purpose:** Define mastery criteria

**Format:**
```markdown
### What You Will Master

By completing this module, you will demonstrate mastery through:

1. **[Skill/Artifact 1]:** [Specific measurable outcome]
2. **[Skill/Artifact 2]:** [Specific measurable outcome]
3. **[Skill/Artifact 3]:** [Specific measurable outcome]

**Portfolio Artifact:** [Name of deliverable] - [One sentence on why it matters]
```

**Example:**
```markdown
### What You Will Master

By completing this module, you will demonstrate mastery through:

1. **Schema Design:** A normalized database schema for an e-commerce platform that handles users, products, orders, and reviews
2. **Query Optimization:** Documentation of three query patterns with before/after performance metrics
3. **Failure Analysis:** A troubleshooting guide identifying five common database anti-patterns and their fixes

**Portfolio Artifact:** E-Commerce Database Design Document - A production-ready schema with rationale that demonstrates your ability to design scalable data systems
```

---

## Four-Lesson Structure

Every module contains exactly four lessons following the **Hook → Understand → Apply → Build** progression.

---

## LESSON 1: Introduction - The Hook

**Purpose:** Engage curiosity and establish the big picture  
**Length:** 400-600 words core content  
**Outcome:** Student understands WHAT they're learning and WHY it matters

### Voice & Persona: David Malan (CS50 Harvard)

**Characteristics:**
- Engaging and enthusiastic without being overwhelming
- Uses storytelling and analogies to explain concepts
- Focuses on big picture before diving into details
- Makes technical topics feel accessible and exciting
- Asks "what if" questions to spark curiosity

**Tone Guidelines:**
- Energy level: 7/10 (enthusiastic but not exhausting)
- Use analogies from everyday life (cooking, construction, sports)
- Speak directly to the student ("You've probably experienced...")
- Show genuine excitement about the subject
- Use rhetorical questions to guide thinking

### Content Structure

#### 1. Opening Hook (80-120 words)

Start with one of these proven patterns:

**Pattern A: The Frustration**
> "Picture this: You've built a beautiful app. Everything works locally. You deploy to production and within hours, your database grinds to a halt. Queries that took milliseconds now take seconds. Users are complaining. Your CPU is maxed out. What happened?"

**Pattern B: The Contrast**
> "Two developers build the same feature. One finishes in an afternoon, ships to production, and the system hums along perfectly. The other spends a week, deploys, and immediately faces performance issues. What separates them? It's not coding skill—it's database design."

**Pattern C: The Question**
> "What if I told you that the difference between a database that handles 100 users and one that handles 100 million users isn't complex code—it's three fundamental design decisions made on day one?"

#### 2. The Big Picture (120-180 words)

Establish the mental model using the Malan approach:

**Structure:**
1. Define the concept in one sentence
2. Provide an everyday analogy
3. Connect to real-world technical application
4. Preview the key insight

**Example:**
> "Database design is like city planning. A city planner doesn't just place buildings randomly—they think about traffic flow, utility access, and future growth. Similarly, database design isn't about creating tables—it's about structuring data so information flows efficiently and the system can grow.
>
> Think about your email inbox. Gmail handles billions of messages, yet finding an email from last year takes milliseconds. That's not magic—it's intentional database design. They've structured the data so common queries (recent emails, specific sender) are lightning fast, while rare queries (every email containing a specific word from 2010) can take a bit longer.
>
> The secret? They designed for their most common use cases first. And that's exactly what you'll learn to do."

#### 3. The Technical Foundation (150-250 words)

Introduce the core technical concepts, but keep it at the "what" level, not the "how."

**Guidelines:**
- Define 2-3 key terms in plain English
- Use the formula: Context → Plain English → Analogy → Example
- Avoid implementation details (save for Lesson 2)
- Focus on principles, not syntax

**Example:**
> "Let's establish three foundational concepts:
>
> **1. Schema: Your Data Blueprint**  
> A schema is your database's blueprint. Just like architectural blueprints define where walls, doors, and wiring go, your schema defines what data you store and how it connects. A user table might have email, password, and signup date. A products table has name, price, and inventory. The schema is the contract.
>
> **2. Relationships: How Data Connects**  
> Data doesn't exist in isolation. Users place orders. Orders contain products. Products have reviews. These connections—relationships—are how you structure complex information. Get the relationships wrong, and you'll be rewriting your entire database when requirements change.
>
> **3. Normalization: Avoiding Duplication**  
> Imagine storing a customer's address with every order. When they move, you'd have to update hundreds of records. Normalization means storing each piece of information once and connecting it where needed. It's efficiency through organization."

#### 4. The Preview (80-120 words)

Set expectations for the learning journey.

**Template:**
> "In this module, we'll follow [Hero Name], a developer building [specific project]. You'll see [him/her/them]:
> - [First challenge they face]
> - [Second challenge they face]
> - [How they solve it using the concepts]
>
> By Lesson 4, you'll design your own [deliverable] that demonstrates these principles in action. But first, we need to understand the mechanics. Let's dive deeper."

### Quality Checklist - Lesson 1
- [ ] Opens with compelling hook (frustration/contrast/question)
- [ ] Includes at least one strong analogy
- [ ] Defines 2-3 core terms in plain English
- [ ] Introduces the module's hero character
- [ ] Previews the learning journey
- [ ] Word count: 400-600 words
- [ ] Energy: Engaging without overwhelming
- [ ] Zero implementation code (conceptual only)

---

## LESSON 2: Understanding - The Deep Dive

**Purpose:** Build technical understanding with clear explanations and examples  
**Length:** 600-800 words core content  
**Outcome:** Student can explain concepts and recognize them in practice

### Voice & Persona: Andrew Ng (Stanford)

**Characteristics:**
- Clear, straightforward explanations
- Breaks complex ideas into simple components
- Uses concrete examples before abstractions
- Patient and systematic approach
- "Let's look at an example" as a signature move

**Tone Guidelines:**
- Energy level: 5/10 (calm, focused, authoritative)
- Precise language with defined terms
- Step-by-step progression
- Frequent examples that build on each other
- No unnecessary complexity

### Content Structure

#### 1. Core Concept Breakdown (200-300 words)

Present the main technical concept with surgical clarity.

**Structure:**
1. One-sentence definition
2. Why it matters (2-3 sentences)
3. The mechanism (how it works)
4. Common misconceptions

**Example:**
> "**Database Normalization: Structured Efficiency**
>
> Normalization is the process of organizing data to minimize redundancy and dependency. Instead of repeating information across multiple records, you store each piece of data once and reference it where needed.
>
> Why does this matter? First, it saves storage space. Second, and more importantly, it ensures data consistency. If a customer's email changes, you update one record, not fifty. Third, it makes your queries more predictable and maintainable.
>
> Here's how it works: You identify entities (users, products, orders), define their attributes (what information they contain), and establish relationships (how they connect). Each entity becomes a table. Each attribute becomes a column. Relationships use foreign keys—references to records in other tables.
>
> Common misconception: 'Normalization makes queries slower because you have to join tables.' Reality: Proper indexing makes joins extremely fast, and the consistency benefits far outweigh the minimal performance cost for most applications."

#### 2. Concrete Examples (250-400 words)

Provide 2-3 progressive examples that build understanding.

**Pattern:** Basic → Typical → Edge Case

**Example:**

> "**Example 1: E-Commerce Orders (Basic)**
>
> Let's say we're tracking orders. A non-normalized approach might look like:
>
> ```
> Orders Table:
> order_id | customer_name | customer_email | product_name | product_price | quantity
> 1001     | Alice Chen    | alice@mail.com | USB Cable    | 12.99        | 2
> 1002     | Alice Chen    | alice@mail.com | Phone Case   | 24.99        | 1
> ```
>
> Notice the problem? Alice's information is duplicated. If she changes her email, we'd have to update multiple rows.
>
> The normalized version splits this into three tables:
>
> ```
> Customers:
> customer_id | name       | email
> 500         | Alice Chen | alice@mail.com
>
> Products:
> product_id | name       | price
> 200        | USB Cable  | 12.99
> 201        | Phone Case | 24.99
>
> Orders:
> order_id | customer_id | product_id | quantity
> 1001     | 500         | 200        | 2
> 1002     | 500         | 201        | 1
> ```
>
> Now Alice exists once. Products exist once. Orders simply reference them.
>
> **Example 2: Handling Changes (Typical)**
>
> When Alice updates her email:
> - Non-normalized: Update every order row → Multiple queries, risk of inconsistency
> - Normalized: Update one customer row → Single query, guaranteed consistency
>
> When a product price changes:
> - Non-normalized: Historical orders show wrong prices (or you can't update the price)
> - Normalized: Historical orders preserve the price at time of purchase (add price to orders table), current price lives in products table"

#### 3. Technical Details with Pseudocode (150-200 words)

Show the mechanics without overcomplicating.

**Guidelines:**
- Use pseudocode or simplified SQL
- Add inline comments explaining each step
- Focus on the pattern, not perfect syntax
- Connect code to concepts

**Example:**

> "**Creating Relationships: Foreign Keys**
>
> A foreign key is a reference to a record in another table. Here's the pattern:
>
> ```sql
> -- Create the parent table first
> CREATE TABLE customers (
>   customer_id INT PRIMARY KEY,  -- Unique identifier
>   name VARCHAR(100),
>   email VARCHAR(100)
> );
>
> -- Then create the child table with reference
> CREATE TABLE orders (
>   order_id INT PRIMARY KEY,
>   customer_id INT,              -- Reference to customers
>   order_date DATE,
>   FOREIGN KEY (customer_id) 
>     REFERENCES customers(customer_id)  -- Establishes the link
> );
> ```
>
> The foreign key constraint ensures data integrity. You cannot create an order for a customer that doesn't exist. If you try to delete a customer who has orders, the database prevents it (or handles it according to your rules)."

#### 4. Common Patterns & Variations (100-150 words)

Introduce the most important patterns students will encounter.

**Example:**

> "**Three Essential Relationship Patterns**
>
> 1. **One-to-Many:** One customer has many orders. Most common pattern. Use a foreign key in the 'many' table.
>
> 2. **Many-to-Many:** One order can have many products. One product can be in many orders. Requires a junction table (order_items) that connects both.
>
> 3. **One-to-One:** One user has one profile. Rare but useful for separating frequently-accessed data from rarely-accessed data.
>
> Understanding these three patterns solves 95% of data modeling challenges."

### Quality Checklist - Lesson 2
- [ ] Concepts defined with precision
- [ ] 2-3 progressive examples (basic → typical → edge case)
- [ ] Includes pseudocode or simplified code with comments
- [ ] Addresses one common misconception
- [ ] Covers essential patterns
- [ ] Word count: 600-800 words
- [ ] Tone: Patient, systematic, clear
- [ ] Every technical term is defined

---

## LESSON 3: Application - The Case Study

**Purpose:** Show real-world application and impact through narrative  
**Length:** 500-700 words core content  
**Outcome:** Student sees how concepts solve actual problems

### Voice & Persona: Robin Williams (Good Will Hunting / Dead Poets Society)

**Characteristics:**
- Warm, engaging, and occasionally humorous
- Balances professionalism with personality
- Uses storytelling to make points memorable
- Asks provocative "what if" questions
- Focuses on human impact and meaning

**Tone Guidelines:**
- Energy level: 6/10 (engaging, conversational, warm)
- Use personality and light humor where appropriate
- Tell stories that reveal deeper truths
- Make the "so what" explicit and compelling
- Connect technical decisions to human outcomes

### Content Structure

#### 1. Case Study Setup (120-180 words)

Introduce the hero and their challenge using narrative structure.

**Template:**
> "Meet [Hero Name], [their role] at [company/project type].
>
> [Hero's challenge - the problem they face]
>
> [The stakes - why this matters]
>
> [The constraint - what makes it interesting]"

**Example:**

> "Meet Priya, a backend engineer at a rapidly growing food delivery startup. Three months ago, they had 5,000 users. Now they have 50,000, and her database is starting to creak under the pressure.
>
> The symptom? The 'active orders' page—the most critical feature—takes 8 seconds to load during peak dinner hours. Restaurants are seeing outdated order statuses. Drivers are getting incorrect delivery information. Customer support is overwhelmed.
>
> The twist? Priya's database design isn't technically 'wrong.' It works fine for 5,000 users. But it doesn't scale. And she has two weeks to fix it before their biggest marketing campaign launches.
>
> This is where database design becomes art."

#### 2. The Analysis - What Went Wrong (180-250 words)

Forensically examine the failure with empathy and insight.

**Structure:**
1. Show the problematic approach
2. Explain why it seemed reasonable at the time
3. Identify the hidden cost
4. Connect to core concepts from Lesson 2

**Example:**

> "Let's look at Priya's original design with compassion. She did what made sense:
>
> ```
> active_orders view:
> SELECT orders.*, customers.*, drivers.*, restaurants.*, 
>        menu_items.*, delivery_addresses.*
> FROM orders
> JOIN customers ON orders.customer_id = customers.id
> JOIN drivers ON orders.driver_id = drivers.id
> ... (5 more joins)
> WHERE orders.status = 'in_progress'
> ```
>
> This worked beautifully with 5,000 users. The query took 200ms. Everyone was happy.
>
> But here's what happened at scale: With 50,000 users and 2,000 concurrent active orders, this single query now joins seven tables, touches hundreds of thousands of rows, and returns massive amounts of data—most of which the UI doesn't even display.
>
> The hidden cost? The query requests everything because it was easier to code. Driver's full profile? Retrieved. Customer's complete order history? Retrieved. Menu item's nutritional information? Retrieved. All for a dashboard that shows four fields: order number, customer name, status, and time.
>
> This is the difference between 'works' and 'scales.' Priya's design wasn't wrong for MVP. But it violated a core principle: **Query only what you need**. And at scale, that principle becomes survival."

#### 3. The Solution Journey (200-300 words)

Walk through the solution with insight and teaching moments.

**Guidelines:**
- Show the thinking process, not just the answer
- Highlight key decisions and tradeoffs
- Include "aha" moments
- Connect back to core concepts

**Example:**

> "Priya's solution came from asking one question: 'What does the dashboard actually need?'
>
> Not 'what could it need someday.' Not 'what might be useful.' What does it need right now?
>
> Four fields. That's it.
>
> She created a specialized view:
>
> ```sql
> CREATE VIEW active_orders_dashboard AS
> SELECT 
>   orders.order_number,
>   customers.name,
>   orders.status,
>   orders.created_at
> FROM orders
> JOIN customers ON orders.customer_id = customers.id
> WHERE orders.status = 'in_progress';
> ```
>
> Two tables instead of seven. Four columns instead of forty. And she added a strategic index:
>
> ```sql
> CREATE INDEX idx_orders_active 
> ON orders(status, created_at) 
> WHERE status = 'in_progress';
> ```
>
> This index tells the database: 'Hey, we ask about active orders constantly. Keep a fast path to that data.'
>
> The results? Query time dropped from 8 seconds to 120ms. Under load. During peak hours.
>
> But here's the real lesson: Priya didn't optimize by making the query more clever. She optimized by making the query more honest. She stopped asking for data she didn't need.
>
> Sometimes the best code is the code you don't write. Sometimes the best optimization is the simplest question: 'Do I really need this?'"

#### 4. The Impact & Takeaway (100-150 words)

End with the human impact and broader lesson.

**Example:**

> "**The Results:**
> - Dashboard load time: 8s → 120ms (98% improvement)
> - Database CPU usage: Dropped 60%
> - Customer support tickets about order status: Down 80%
> - Priya's stress level: Significantly lower
>
> **The Deeper Truth:**
> This wasn't just a technical win. It was a mindset shift. Priya stopped optimizing code and started optimizing questions. She stopped building for imaginary future needs and started building for real current needs.
>
> And that's the skill that separates developers who survive scale from developers who struggle with it. It's not about knowing more database tricks. It's about asking better questions about what you're really trying to accomplish.
>
> Which brings us to your turn..."

### Quality Checklist - Lesson 3
- [ ] Compelling hero with clear challenge
- [ ] Analysis explains *why* the original approach failed
- [ ] Solution shows the thinking process
- [ ] Includes specific metrics or outcomes
- [ ] Connects technical decisions to human impact
- [ ] Word count: 500-700 words
- [ ] Tone: Engaging, warm, insightful
- [ ] Contains "aha" moment or deeper lesson

---

## LESSON 4: Activity - The Deliverable

**Purpose:** Hands-on work that produces portfolio-ready artifact  
**Length:** 300-500 words of instruction + structured problem  
**Outcome:** Student creates tangible work demonstrating mastery

### Voice & Persona: CS50 Problem Set Style

**Characteristics:**
- Clear, direct, no-nonsense instructions
- Provides structure without hand-holding
- Includes examples and tips for getting started
- Focuses on specifications and outcomes
- Encourages independent problem-solving

**Tone Guidelines:**
- Energy level: 4/10 (direct, professional, supportive)
- Use bullet points and clear specifications
- Provide enough guidance to start, not solve
- Include quality criteria
- No fluff or unnecessary words

### Content Structure

#### 1. Activity Overview (80-120 words)

State what they're building and why it matters.

**Template:**
```markdown
## Your Task: [Clear Deliverable Name]

In this activity, you will [action verb] [specific artifact] that demonstrates [key skills from module].

**Deliverable:** [Artifact name and format]  
**Time Estimate:** [Realistic time range]  
**Skills Demonstrated:** [3-4 skills]

**Why This Matters:**  
[2-3 sentences connecting this to real work or portfolio value]
```

**Example:**

```markdown
## Your Task: Design an E-Commerce Database Schema

In this activity, you will design a normalized database schema for an e-commerce platform that handles products, customers, orders, and reviews.

**Deliverable:** Database schema document with ERD and table definitions  
**Time Estimate:** 90-120 minutes  
**Skills Demonstrated:** Schema design, normalization, relationship modeling, documentation

**Why This Matters:**  
This is exactly what you'd do on day one of a new backend project. A well-designed schema becomes the foundation for everything else. This artifact demonstrates your ability to structure complex data systems—a skill valued by every tech company.
```

#### 2. Specifications (200-300 words)

Provide clear requirements without prescribing the exact solution.

**Format:**

```markdown
### Requirements

Your schema must include:

**Core Entities:**
1. [Entity 1]: [What it represents and key attributes]
2. [Entity 2]: [What it represents and key attributes]
3. [Entity 3]: [What it represents and key attributes]

**Relationships:**
- [Relationship 1 with justification]
- [Relationship 2 with justification]
- [Relationship 3 with justification]

**Constraints:**
1. [Business rule 1]
2. [Business rule 2]
3. [Business rule 3]

**Documentation:**
- ERD (entity-relationship diagram) showing all tables and relationships
- Table definitions with column names, data types, and constraints
- Brief rationale (2-3 sentences) for key design decisions
```

**Example:**

```markdown
### Requirements

Your schema must include:

**Core Entities:**
1. **Users/Customers**: Store customer account information (name, email, password, registration date)
2. **Products**: Catalog items available for purchase (name, description, price, inventory, category)
3. **Orders**: Purchase transactions (order date, status, total amount)
4. **Order Items**: Individual products within an order (quantity, price at time of purchase)
5. **Reviews**: Customer product reviews (rating, comment, date)

**Relationships:**
- One customer can place many orders (1:M)
- One order contains many products through order items (M:M with junction table)
- One product can have many reviews (1:M)
- One customer can write many reviews (1:M)

**Constraints:**
1. Email addresses must be unique per customer
2. Product prices must be stored with orders to preserve historical pricing
3. Reviews must be linked to both the customer and the product
4. Order status must be one of: pending, processing, shipped, delivered, cancelled

**Documentation:**
- ERD showing all five tables and their relationships
- Table definitions with primary keys, foreign keys, and data types
- Written rationale for your normalization decisions (Why separate order_items? Why store price with each order item?)
```

#### 3. Getting Started (80-120 words)

Provide concrete first steps and tips.

**Example:**

```markdown
### Getting Started

**Step 1: Sketch the Entities**  
On paper or whiteboard, list your five core entities. Under each, write 4-6 attributes you think it needs.

**Step 2: Identify Relationships**  
Draw lines between entities that connect. Ask: "Can one X have many Y?" Label each relationship.

**Step 3: Check for Redundancy**  
Look for repeated information. If you see customer_name in multiple tables, you likely need to normalize.

**Tips:**
- Start with the minimum viable schema. You can always add complexity.
- Remember: Orders and OrderItems are different. Orders is the transaction. OrderItems is the list.
- Use tools like dbdiagram.io or draw.io for your ERD
- Test your design: Write out 2-3 sample queries you'd need to run. Can your schema answer them efficiently?
```

#### 4. Evaluation Criteria (100-150 words)

Show exactly how their work will be assessed.

**Format:**

```markdown
### How You'll Know You're Done

Your schema is complete when:

**Structure (40 points):**
- [ ] All five required entities are present
- [ ] Relationships are correctly defined with foreign keys
- [ ] Junction table properly implements many-to-many relationship
- [ ] Primary keys defined for all tables

**Normalization (30 points):**
- [ ] No repeated customer/product information
- [ ] Historical pricing preserved in order_items
- [ ] Each piece of data stored once

**Documentation (30 points):**
- [ ] ERD clearly shows tables and relationships
- [ ] Table definitions include data types and constraints
- [ ] Written rationale explains key decisions

**Quality Bar:** If you can explain your schema to a developer who's never seen it, and they understand how to query it, you've succeeded.
```

#### 5. Extensions (Optional) (50-80 words)

Offer challenges for students who finish early.

**Example:**

```markdown
### Going Further (Optional)

If you finish early and want to challenge yourself:

1. **Add Inventory Management**: Track product stock levels and handle low-stock alerts
2. **Implement Wish Lists**: Allow customers to save products for later
3. **Add Product Categories**: Create a hierarchical category system (Electronics > Laptops > Gaming Laptops)
4. **Design for Multi-Vendor**: Extend the schema to support multiple sellers, not just one store

These aren't required, but they're great portfolio additions.
```

### Quality Checklist - Lesson 4
- [ ] Clear deliverable with specific format
- [ ] Requirements are detailed but not prescriptive
- [ ] Getting started section provides concrete first steps
- [ ] Evaluation criteria uses checklist format
- [ ] Includes tips for debugging/getting unstuck
- [ ] Optional extensions for advanced students
- [ ] Word count: 300-500 words
- [ ] Tone: Direct, clear, supportive
- [ ] Zero ambiguity about what "done" looks like

---

## Module Completion Standards

### Definition of Done

A module is complete when the student has:

1. **Artifact Produced**: The Lesson 4 deliverable exists and meets specifications
2. **Concepts Explained**: Student can articulate key concepts in their own words
3. **Decisions Justified**: Student can explain their design decisions with rationale
4. **Quality Validated**: Deliverable passes evaluation criteria

### Portfolio Integration

Every module artifact should:
- Be shareable (clean documentation, clear presentation)
- Demonstrate specific technical skills
- Show decision-making process, not just final output
- Be explainable in an interview setting

---

## Cross-Module Hero Consistency

### Hero Character Development

Use **one hero** per module (or one hero per course).

**Hero Profile Template:**
```markdown
**Name:** [Realistic first name]
**Role:** [Relevant job title]
**Context:** [Company type/project type]
**Personality:** [1-2 traits that make them relatable]
```

**Example:**
```markdown
**Name:** Alex
**Role:** Full-stack developer
**Context:** Early-stage startup building a SaaS product
**Personality:** Eager to build quickly but learning to balance speed with quality
```

**Usage Guidelines:**
- Reference the hero by name in Lessons 1, 3
- Show the hero learning and making mistakes
- Have the hero evolve across modules
- Keep the hero relatable, not a superhero developer

---

## Voice Consistency Matrix

| Element | Primary Voice | Energy Level | Key Characteristics |
|:--------|:--------------|:------------|:--------------------|
| Module Introduction | Practical Expert | 7/10 | Clear, engaging, fundamentals-focused |
| North Star | Inspiring Coach | 8/10 | Bold, outcome-focused, motivating |
| Lesson 1 | David Malan | 7/10 | Storytelling, analogies, big picture |
| Lesson 2 | Andrew Ng | 5/10 | Clear, systematic, examples-driven |
| Lesson 3 | Robin Williams | 6/10 | Warm, insightful, human-focused |
| Lesson 4 | CS50 Problem Set | 4/10 | Direct, structured, no-nonsense |
| Module Summary | Confident Validator | 6/10 | Affirming, specific, portfolio-focused |

---

## Anti-Patterns to Avoid

### Content Anti-Patterns
❌ **Info Dumping**: Listing every possible feature without context  
✅ **Progressive Disclosure**: Start simple, layer complexity

❌ **Jargon Without Definition**: Assuming students know technical terms  
✅ **Context-First**: Define terms in plain English on first use

❌ **Perfect Code Only**: Showing flawless solutions without the journey  
✅ **Mistakes → Fixes**: Show the wrong approach, then the right approach

❌ **Passive Voice**: "The database can be queried..."  
✅ **Active Voice**: "You query the database..."

### Structure Anti-Patterns
❌ **Inconsistent Hero**: Different characters each lesson  
✅ **Single Hero Arc**: Same character learning throughout

❌ **Missing Rationale**: "Do this because I said so"  
✅ **Explained Tradeoffs**: "Here's why we choose X over Y"

❌ **Vague Outcomes**: "Understand databases"  
✅ **Specific Artifacts**: "Design a normalized e-commerce schema"

### Tone Anti-Patterns
❌ **Talking Down**: "This is simple..."  
✅ **Respectful**: "This concept builds on..."

❌ **Overwhelming**: Excessive enthusiasm or complexity  
✅ **Calibrated**: Match energy to content density

❌ **Inconsistent Formality**: Mixing very casual with very formal  
✅ **Professional-Friendly**: Consistent warm professionalism

---

## Adaptation Guidelines

### For Different Subjects

**For CS Fundamentals** (Algorithms, Data Structures):
- Emphasize the "why" behind each data structure
- Use performance comparisons and Big O notation in Lesson 2
- Case studies should show real-world performance implications

**For AI/ML Courses**:
- Lesson 1: Focus on intuition before mathematics
- Lesson 2: Balance theory with code examples
- Lesson 3: Show both successes and failures of AI systems

**For Web Development**:
- Include visual examples (screenshots, mockups)
- Lesson 2: Show both backend and frontend perspective
- Lesson 4: Working prototype, not just code

**For Agentic Engineering**:
- Emphasize contracts and specifications
- Show AI collaboration patterns
- Case studies include prompt engineering evolution

### For Different Audiences

**Beginners:**
- More analogies in Lesson 1
- Shorter code examples in Lesson 2
- More detailed getting-started steps in Lesson 4

**Intermediate:**
- Standard template as-is
- Include "why this approach" rationale
- Extensions in Lesson 4 are important

**Advanced:**
- Lesson 1 can be condensed
- Lesson 2 should include edge cases and tradeoffs
- Lesson 4 should have challenging specifications

---

## Quality Assurance Checklist

### Module-Level
- [ ] North Star statement is specific and outcome-focused
- [ ] Three learning objectives follow Bloom's taxonomy
- [ ] Module intro is 200-400 words with clear hook
- [ ] Module summary defines portfolio artifact
- [ ] One hero character used consistently

### Lesson-Level
- [ ] Lesson 1: Engaging hook, big picture, analogies present
- [ ] Lesson 2: Concepts defined clearly, examples progress from basic to complex
- [ ] Lesson 3: Case study has problem, analysis, solution, impact
- [ ] Lesson 4: Clear specifications, getting started guide, evaluation criteria

### Voice/Tone
- [ ] Each lesson matches its designated voice persona
- [ ] Energy levels appropriate to content density
- [ ] Technical terms defined on first use
- [ ] No jargon without context
- [ ] Active voice used throughout

### Practical Standards
- [ ] Every concept includes rationale
- [ ] Code examples include comments
- [ ] Anti-patterns explicitly called out
- [ ] Deliverable is portfolio-ready
- [ ] Assessment criteria are measurable

---

## Version History

**v2.0** - Comprehensive master template for all technical courses  
**v1.0** - Initial agentic-focused template

---

## Template Metadata

**Maintained By:** Bradley, The Architect of Agents  
**Use Cases:** CS courses, technical bootcamps, AI/ML education, professional development  
**Target Outcome:** Students who can build, explain, and improve technical systems  
**Philosophy:** You lead. The AI/tools support. Outcomes over theory.

---

*This template is designed to be used by human course designers and AI agents creating educational content. It prioritizes practical skills, clear communication, and portfolio-ready outcomes.*
