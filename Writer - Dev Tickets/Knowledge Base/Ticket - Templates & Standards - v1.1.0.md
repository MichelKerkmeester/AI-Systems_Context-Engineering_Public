# Ticket - Templates & Standards - v1.1.0

Comprehensive templates, symbols, and formatting standards for all ticket types. This is the single source of truth for ticket structure.

## Table of Contents

1. [📋 ARTIFACT STANDARDS](#1--artifact-standards)
2. [🔤 SYMBOL REFERENCE](#2--symbol-reference)
3. [📐 BASE TEMPLATES BY MODE](#3--base-templates-by-mode)
4. [✅ RESOLUTION CHECKLIST TEMPLATES](#4--resolution-checklist-templates)
5. [📝 FORMATTING STANDARDS](#5--formatting-standards)
6. [🎯 SECTION TEMPLATES](#6--section-templates)

---

## 1. 📋 ARTIFACT STANDARDS

### Critical Requirements

**🚨 CRITICAL:** Always use `text/markdown` artifact type when delivering structured content!

Never use `text/plain` for content with markdown formatting. This causes raw markdown to display instead of formatted text.

### Mandatory Header

Every ticket artifact MUST start with:

```markdown
MODE: [mode used]
TICKET TYPE: [Feature/Bug/Improvement/Epic]
MCP USED: [Sequential Thinking/Cascade Thinking/Figma/Multiple/None Available]
```

### Standard Structure

```markdown
MODE: $s
TICKET TYPE: Feature
MCP USED: Sequential Thinking

---

[Ticket content follows standard template]
```

---

## 2. 🔤 SYMBOL REFERENCE

### Primary Section Symbols (Required)
- **❖** - Title and major feature sections
- **⌘** - About/contextual sections
- **◇** - Process/workflow sections and requirements
- **→** - Designs & References sections
- **✓** - Success criteria sections AND Resolution Checklist
- **⊗** - Dependencies or out of scope
- **⚠** - Risks and important notices

### Secondary/Nested Symbols
- **◻︎** - Specific items/components within categories
- **◆** - Alternative major section marker
- **◈** - Document section headers
- **▸** - Sub-items or progressive disclosure
- **•** - Bullet points under items

### Callout Mapping
| Symbol | Section Type | Callout Type | Purpose |
|--------|-------------|--------------|---------|
| ❖ | Title/Feature | NOTE | Primary feature identification |
| ◇ | Requirements | IMPORTANT | Core requirements emphasis |
| → | Designs/References | INFO | Supporting information |
| ✓ | Success/Checklist | TIP | Actionable items |
| ⊗ | Dependencies | WARNING | Blocking/blocked items |
| ⚠ | Risks | CAUTION | Risk awareness |
| ⌘ | About/Context | NOTE | Background information |

### Symbol Hierarchy Example
```markdown
> [!NOTE]
> ### ❖ Improvement: [Enhancement Description]
> 
> **User Value:** [How this improves user experience]
> 
> **Business Goal:** [Measurable improvement target]

---

> [!INFO]
> ## ◈ Current State
> - [Current metric/behavior]
> - [Pain points]

---

> [!TIP]
> ## ◆ Target State
> - [Improved metric/behavior]
> - [Benefits achieved]

---

> [!IMPORTANT]
> ## ◇ Requirements
> - [Improvement requirement 1]
> - [Improvement requirement 2]
> - [Measurement implementation]

---

> [!TIP]
> ## ✓ Success Criteria
> - [ ] [Performance target met]
> - [ ] [User metric improved]
> - [ ] [No negative side effects]

---

> [!TIP]
> ## ✓ Resolution Checklist
> 
> ### Analysis
> - [ ] Baseline measurements taken
> - [ ] Improvement targets defined
> - [ ] Impact assessment complete
> 
> ### Implementation
> - [ ] Apply optimizations
> - [ ] Update related systems
> - [ ] Add monitoring
> 
> ### Validation
> - [ ] Measure improvements
> - [ ] Compare to targets
> - [ ] Document results]
> ### ❖ Main Feature

> [!IMPORTANT]
> ## ◇ Requirements
> 
> ### ◻︎ Component A
> - Requirement 1
> - Requirement 2
> 
> ### ◻︎ Component B
> - Requirement 3
> - Requirement 4
```

---

## 3. 📐 BASE TEMPLATES BY MODE

### 🚀 Quick Mode ($q) Template

```markdown
MODE: $q
TICKET TYPE: Feature
MCP USED: Sequential Thinking

---

> [!NOTE]
> ### ❖ [Feature Name]
> 
> **User Value:** [One-line user benefit]
> 
> **Business Goal:** [Specific metric improvement]

---

> [!IMPORTANT]
> ## ◇ Requirements
> - [Requirement 1]
> - [Requirement 2]
> - [Requirement 3]

---

> [!TIP]
> ## ✓ Success Criteria
> - [ ] [Criterion 1]
> - [ ] [Criterion 2]
> - [ ] [Criterion 3]

---

> [!TIP]
> ## ✓ Resolution Checklist
> - [ ] [Implementation task 1]
> - [ ] [Implementation task 2]
> - [ ] [Testing task]
> - [ ] [Mobile verification]
> - [ ] [Code review]
```

### 📋 Standard Mode ($s) Template

```markdown
MODE: $s
TICKET TYPE: Feature
MCP USED: Sequential Thinking

---

> [!NOTE]
> ### ❖ [Feature Name]
> 
> **User Value:** [Detailed user benefit]
> 
> **Business Goal:** [Measurable business outcome with metrics]

---

> [!IMPORTANT]
> ## ◇ Requirements
> 
> **[Category 1]**
> - [Detailed requirement]
> - [Another requirement]
> 
> **[Category 2]**
> - [More requirements]
> - [Edge case handling]

---

> [!INFO]
> ## → Designs & References
> - [Figma - Main Flow](link)
> - [API Documentation](link)
> 
> **Notice:** [Important implementation note]

---

> [!TIP]
> ## ✓ Success Criteria
> - [ ] [Detailed criterion 1]
> - [ ] [Performance metric]
> - [ ] [User experience metric]
> - [ ] [Business metric]

---

> [!TIP]
> ## ✓ Resolution Checklist
> 
> ### Implementation
> - [ ] [Core feature task 1]
> - [ ] [Core feature task 2]
> - [ ] [API integration]
> 
> ### Testing & QA
> - [ ] [Unit tests]
> - [ ] [Integration tests]
> - [ ] [Cross-browser testing]
> 
> ### Documentation
> - [ ] [Code documentation]
> - [ ] [API updates]

---

> [!WARNING]
> ## ⊗ Dependencies
> - Requires: [Backend API] (#1234)
> - Blocks: [Next feature] (#1235)
```

### 🔧 Complex Mode ($c) Template

```markdown
MODE: $c
TICKET TYPE: Feature
MCP USED: Cascade Thinking

---

> [!NOTE]
> ### ❖ [Complex Feature Name]

---

> [!NOTE]
> # ⌘ About
> 
> [2-3 paragraphs explaining context and strategic importance]
> 
> **User Value:** [Comprehensive user benefit]
> 
> **Business Goal:** [Strategic outcome with metrics]

---

[[*TOC*]]

---

> [!INFO]
> ## → Designs & References
> 
> ### ◻︎ User Flows
> - [Figma - Complete Journey](link)
> - [Figma - Edge Cases](link)
> 
> ### ◻︎ Technical Architecture
> - [Architecture Diagram](link)
> - [API Specification](link)

---

> [!IMPORTANT]
> ## ◇ Phase 1: [Foundation] (Timeline)
> - [Foundation element 1]
> - [Foundation element 2]
> - [Basic functionality]

---

> [!IMPORTANT]
> ## ◇ Phase 2: [Core Features] (Timeline)
> - [Main feature 1]
> - [Main feature 2]
> - [Integration points]

---

> [!IMPORTANT]
> ## ◇ Phase 3: [Enhancement] (Timeline)
> - [Advanced features]
> - [Polish and refinement]
> - [Final testing]

---

> [!TIP]
> ## ✓ Success Criteria
> - [ ] [High-level metric 1]
> - [ ] [Performance benchmark]
> - [ ] [User adoption metric]
> - [ ] [Business impact metric]

---

> [!TIP]
> ## ✓ Resolution Checklist
> 
> ### Phase 1: Foundation
> - [ ] [Infrastructure setup]
> - [ ] [Basic components]
> - [ ] [Initial testing]
> - [ ] [Phase 1 demo]
> 
> ### Phase 2: Core Features
> - [ ] [Feature implementation]
> - [ ] [Integration complete]
> - [ ] [Performance optimization]
> - [ ] [Phase 2 review]
> 
> ### Phase 3: Enhancement
> - [ ] [Advanced features]
> - [ ] [UI/UX polish]
> - [ ] [Final testing]
> - [ ] [Production ready]
> 
> ### Launch Preparation
> - [ ] [Security review]
> - [ ] [Monitoring configured]
> - [ ] [Rollback plan]
> - [ ] [Team handoff]

---

> [!WARNING]
> ## ⊗ Dependencies
> - Requires: [Major dependency 1] (#3001)
> - Blocks: [Future initiative] (#3100)

---

> [!CAUTION]
> ## ⚠ Risks
> - **[Risk 1]:** [Description and mitigation]
> - **[Risk 2]:** [Description and mitigation]
```

### 🚀 Epic Mode ($e) Template

```markdown
MODE: $e
TICKET TYPE: Epic
MCP USED: Cascade Thinking

---

> [!NOTE]
> ### ❖ Epic: [Epic Title]
> 
> **User Value:** [High-level user outcome]
> 
> **Business Goal:** [Strategic business objective]

---

> [!NOTE]
> ## ⌘ Overview
> [1-2 paragraphs describing scope and importance]

---

> [!TIP]
> ## ✓ Success Metrics
> - [ ] [Epic-level metric 1]
> - [ ] [Epic-level metric 2]
> - [ ] [Epic-level metric 3]

---

> [!IMPORTANT]
> ## ◇ Child Tickets
> 
> ### ◻︎ Phase 1: [Foundation]
> - [ ] **[Ticket 1]** - [Brief description]
> - [ ] **[Ticket 2]** - [Brief description]
> 
> ### ◻︎ Phase 2: [Core]
> - [ ] **[Ticket 3]** - [Brief description]
> - [ ] **[Ticket 4]** - [Brief description]
> 
> ### ◻︎ Phase 3: [Enhancement]
> - [ ] **[Ticket 5]** - [Brief description]
> - [ ] **[Ticket 6]** - [Brief description]

---

> [!TIP]
> ## ✓ Resolution Checklist
> 
> ### Epic Coordination
> - [ ] All child tickets created
> - [ ] Team assignments complete
> - [ ] Timeline established
> - [ ] Success metrics dashboard
> 
> ### Cross-Cutting Concerns
> - [ ] Design consistency verified
> - [ ] API contracts finalized
> - [ ] Security review scheduled
> - [ ] Performance targets set
> 
> ### Launch Readiness
> - [ ] Beta testing complete
> - [ ] Documentation ready
> - [ ] Support team trained
> - [ ] Go-live plan approved

---

> [!WARNING]
> ## ⊗ Dependencies
> - Requires: [Strategic prerequisite] (#5001)

---

> [!NOTE]
> ## ⌘ Timeline
> [Total timeline with phase breakdowns]
```

### 🐛 Bug Template

```markdown
MODE: $s
TICKET TYPE: Bug
MCP USED: Sequential Thinking

---

> [!NOTE]
> ### ❖ Bug: [Issue Description]
> 
> **User Value:** [What gets fixed for users]
> 
> **Business Goal:** [Why this fix matters]

---

> [!IMPORTANT]
> ## ◆ Current Behavior
> [What's happening now - the bug]

---

> [!TIP]
> ## ✓ Expected Behavior
> [What should happen instead]

---

> [!INFO]
> ## ◈ Steps to Reproduce
> 1. [Step 1]
> 2. [Step 2]
> 3. [Observe bug]

---

> [!INFO]
> ## → Evidence
> - [Screenshot - Bug](link)
> - [Error logs](link)

---

> [!TIP]
> ## ✓ Success Criteria
> - [ ] Bug no longer reproducible
> - [ ] No regression in related features
> - [ ] Works across all supported browsers

---

> [!TIP]
> ## ✓ Resolution Checklist
> 
> ### Investigation
> - [ ] Reproduce bug locally
> - [ ] Identify root cause
> - [ ] Check for related issues
> 
> ### Fix Implementation
> - [ ] Implement fix
> - [ ] Verify bug resolved
> - [ ] Add regression test
> 
> ### Verification
> - [ ] Test on all browsers
> - [ ] Deploy to staging
> - [ ] Monitor for 24 hours
```

### 📈 Improvement Template

```markdown
MODE: $s
TICKET TYPE: Improvement
MCP USED: Sequential Thinking

---

> [!NOTE]
> ### ❖ Improvement: [Enhancement Description]
> 
> **User Value:** [How this improves user experience]
> 
> **Business Goal:** [Measurable improvement target]

---

> [!INFO]
> ## ◈ Current State
> - [Current metric/behavior]
> - [Pain points]

---

> [!TIP]
> ## ◆ Target State
> - [Improved metric/behavior]
> - [Benefits achieved]

---

> [!IMPORTANT]
> ## ◇ Requirements
> - [Improvement requirement 1]
> - [Improvement requirement 2]
> - [Measurement implementation]

---

> [!TIP]
> ## ✓ Success Criteria
> - [ ] [Performance target met]
> - [ ] [User metric improved]
> - [ ] [No negative side effects]

---

> [!TIP]
> ## ✓ Resolution Checklist
> 
> ### Analysis
> - [ ] Baseline measurements taken
> - [ ] Improvement targets defined
> - [ ] Impact assessment complete
> 
> ### Implementation
> - [ ] Apply optimizations
> - [ ] Update related systems
> - [ ] Add monitoring
> 
> ### Validation
> - [ ] Measure improvements
> - [ ] Compare to targets
> - [ ] Document results
```

---

## 4. ✅ RESOLUTION CHECKLIST TEMPLATES

### Sizing by Mode

| Mode | Items | Structure | Focus |
|------|-------|-----------|-------|
| **Quick ($q)** | 3-5 | Single list | Essential tasks |
| **Standard ($s)** | 8-15 | 2-3 categories | Balanced coverage |
| **Complex ($c)** | 15-30 | Phase-based | Progressive work |
| **Epic ($e)** | 10-20 | Coordination | High-level tasks |

### Category Templates

**Implementation Category**
```markdown
### Implementation
- [ ] Build UI components per design
- [ ] Implement business logic
- [ ] Connect to backend APIs
- [ ] Add error handling
- [ ] Implement state management
```

**Testing Category**
```markdown
### Testing & QA
- [ ] Write unit tests (>80% coverage)
- [ ] Create integration tests
- [ ] Test on all browsers
- [ ] Verify mobile responsiveness
- [ ] Performance testing
```

**Documentation Category**
```markdown
### Documentation
- [ ] Update API documentation
- [ ] Add inline code comments
- [ ] Update team wiki
- [ ] Create user guide
- [ ] Document configuration
```

**Deployment Category**
```markdown
### Deployment
- [ ] Update deployment scripts
- [ ] Configure environment variables
- [ ] Set up monitoring
- [ ] Create rollback plan
- [ ] Verify in staging
```

### SMART Criteria for Checklist Items

Every item should be:
- **S**pecific - Clear what needs to be done
- **M**easurable - Can mark as complete or not
- **A**ctionable - Developer knows how to start
- **R**elevant - Contributes to ticket completion
- **T**ime-bound - Fits within ticket scope

---

## 5. 📝 FORMATTING STANDARDS

### Section Dividers
Always use `---` between ALL major sections

### Callout Usage
- Each major section header must be wrapped in an appropriate callout
- Use the callout mapping from Section 2
- Content within callouts maintains standard formatting

### Text Formatting
- **Bold** for emphasis and key terms
- *Italics* sparingly for subtle emphasis
- `Code` for technical terms
- NEVER use em dashes (—, –, or --)

### Links
```markdown
[Descriptive Text](url)
[Figma - Component Name](figma-url)
[API Documentation](api-url)
```

### Lists
- Use `-` for unordered lists
- Use `1.` for ordered lists
- Use `- [ ]` for checkboxes
- Indent with 2 spaces for nested items

### Arrows & Flow
- Use `→` for cause/effect or flow
- Example: `User clicks → Modal opens`

### Notices
```markdown
**Notice:** Important information that could be missed
```

---

## 6. 🎯 SECTION TEMPLATES

### Requirements Patterns

**Simple Requirements**
```markdown
> [!IMPORTANT]
> ## ◇ Requirements
> - Clear requirement 1
> - Clear requirement 2
> - Clear requirement 3
```

**Categorized Requirements**
```markdown
> [!IMPORTANT]
> ## ◇ Requirements
> 
> **User Interface**
> - UI requirement 1
> - UI requirement 2
> 
> **Functionality**
> - Functional requirement 1
> - Functional requirement 2
> 
> **Performance**
> - Must load in <2 seconds
> - Support 1000 concurrent users
```

**Flow-Based Requirements**
```markdown
> [!IMPORTANT]
> ## ◇ Requirements
> - **User uploads file** → System validates format
> - **Validation fails** → Show specific error message
> - **Validation passes** → Process and store file
```

### Success Criteria Patterns

Always use checkboxes and be specific:

```markdown
> [!TIP]
> ## ✓ Success Criteria
> - [ ] Feature works as designed on all devices
> - [ ] Page loads in under 2 seconds
> - [ ] 90% of users complete task successfully
> - [ ] Zero critical bugs in production
> - [ ] Analytics tracking implemented
```

### Designs & References Section

```markdown
> [!INFO]
> ## → Designs & References
> 
> ### ◻︎ Design Files
> - [Figma - Desktop Flow](link)
> - [Figma - Mobile Flow](link)
> 
> ### ◻︎ Technical Documentation
> - [API Specification](link)
> - [Database Schema](link)
> 
> **Notice:** Mobile uses different navigation pattern
```

---

*This document is the single source of truth for all ticket templates and standards. Reference specific sections using anchors like `Ticket - Templates & Standards.md#quick-mode` or `Ticket - Templates & Standards.md#symbols`.*