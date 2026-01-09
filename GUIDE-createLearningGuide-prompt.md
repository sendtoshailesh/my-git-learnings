# createLearningGuide - Universal Prompt for Learning Guides

## Overview

`createLearningGuide` is a universal, reusable prompt that generates comprehensive, structured learning guides for technical topics. It works with any LLM (Large Language Model) or AI assistant and is designed to be portable across environments, tools, and projects.

---

## Purpose

Create standardized, high-quality learning guides for any technical topic with:
- Visual diagrams (Mermaid)
- Code examples and cheatsheets
- Real-world scenarios
- Best practices
- Interview/exam preparation materials
- Summary tables and decision trees

---

## How to Use

### With Any LLM or AI Assistant

Copy the prompt template from this guide and paste it into:
- ✅ ChatGPT (OpenAI)
- ✅ Claude (Anthropic)
- ✅ Gemini (Google)
- ✅ Copilot (Microsoft)
- ✅ Any other LLM or AI service

**Basic Usage:**
1. Copy the full prompt template (see Prompt Template section below)
2. Replace `${the specified technical topic}` with your actual topic
3. Paste into your AI assistant chat
4. Submit and get your comprehensive learning guide

**Examples:**
```
Create a comprehensive learning guide for "Merge Conflicts & Resolution" following this standardized structure:
[prompt text...]

Create a comprehensive learning guide for "Docker Containers" following this standardized structure:
[prompt text...]

Create a comprehensive learning guide for "GitHub Actions & CI/CD" following this standardized structure:
[prompt text...]
```

---

## Prompt Template

### Name
`createLearningGuide`

### Description
Create comprehensive learning guide for technical topics with diagrams, examples, and assessment materials.

### Argument Hint
The technical topic or concept to create a learning guide for (e.g., "Docker containers", "API design patterns", "Kubernetes networking")

### Full Prompt Text

```
Create a comprehensive learning guide for "${the specified technical topic}" following this standardized structure:

## Structure to Follow:

1. **Overview Section**
   - Clear definition of the topic
   - Why it matters
   - Main use cases

2. **Core Concepts & Fundamentals**
   - Break down key concepts
   - Use Mermaid diagrams for relationships, flows, and architectures
   - Include visual comparisons when applicable
   - Show interactions between components

3. **Detailed Breakdown Sections**
   - Explain each major concept in depth
   - Provide practical examples
   - Include code snippets or command examples
   - Use comparison tables for features/attributes
   - Show best practices vs anti-patterns

4. **Quick Cheatsheet**
   - Essential commands or syntax
   - Common operations with examples
   - Decision trees for choosing between options
   - Reference tables for quick lookup

5. **Real-World Scenarios (3-4 examples)**
   - Practical use case examples
   - Include workflow diagrams for each scenario
   - Show step-by-step process
   - Relevant to different user types or skill levels

6. **Best Practices Section**
   - Do's and don'ts comparison
   - Common pitfalls to avoid
   - Naming conventions or standards
   - Performance considerations

7. **Interview & Exam Preparation**
   - 10-15 common questions with concise answers
   - Key points to remember for each
   - Scenario-based questions
   - Comparison questions (when to use X vs Y)

8. **Summary & Key Takeaways**
   - 5-10 main takeaways
   - Decision trees for common decisions
   - Quick reference summary table

## Formatting Requirements:

- Use Mermaid diagrams for complex concepts (flows, architectures, relationships)
- Use markdown tables for comparisons and reference material
- Use code blocks with syntax highlighting for technical examples
- Add emoji icons for visual scanning and clarity
- **Use color-coded styling in diagrams with PROPER TEXT CONTRAST:**
  - Success/Green backgrounds: `fill:#4caf50,color:#fff` (white text on green)
  - Error/Red backgrounds: `fill:#f44336,color:#fff` (white text on red)
  - Warning/Orange backgrounds: `fill:#ff9800,color:#fff` (white text on orange)
  - Info/Blue backgrounds: `fill:#2196f3,color:#fff` (white text on blue)
  - Light backgrounds (info): `fill:#e3f2fd,color:#0d47a1` (dark blue text on light blue)
  - Light backgrounds (success): `fill:#e8f5e9,color:#1b5e20` (dark green text on light green)
  - Light backgrounds (warning): `fill:#fff3e0,color:#e65100` (dark orange text on light orange)
  - Light backgrounds (error): `fill:#ffebee,color:#b71c1c` (dark red text on light red)
  - Light backgrounds (purple): `fill:#f3e5f5,color:#4a148c` (dark purple text on light purple)
- **Ensure text color is explicitly specified in all style statements: `style NodeName fill:#color,color:#textcolor`**
- Include clear section breaks with --- dividers
- Make content scannable with bold text and bullet points

## Content Quality Guidelines:

- Explain the "why" not just the "what"
- Include practical, real-world examples
- Keep explanations concise but complete
- Assume reader has basic technical knowledge
- Make it suitable for both learning and exam preparation
- Include common misconceptions and clarifications
```

---

## What You Get

Each generated guide includes:

| Section | Purpose |
|---------|---------|
| **Overview** | Quick introduction & context |
| **Visual Diagrams** | Mermaid diagrams showing relationships & flows |
| **Core Concepts** | Foundational understanding |
| **Detailed Breakdown** | In-depth explanations with examples |
| **Quick Cheatsheet** | Commands, syntax, quick reference |
| **Real-World Scenarios** | 3-4 practical examples with diagrams |
| **Best Practices** | Do's & don'ts, naming conventions |
| **Interview Prep** | Q&A for exams & interviews |
| **Summary** | Key takeaways & decision trees |

---

## Installation & Portability

### Not Required

This prompt **requires no installation**. It's text-based and universal:

1. ✅ Copy the prompt template from this guide
2. ✅ Paste into any AI assistant or LLM
3. ✅ Replace the topic placeholder
4. ✅ Get your learning guide
5. ✅ Share the guide or this documentation anywhere

### Sharing with Teams

- Save this document in your project repository
- Share with team members
- Everyone can generate guides consistently using the same prompt
- No tool-specific setup needed

### Cross-Platform Usage

Works with:
- Web-based AI services (ChatGPT, Gemini, Claude web)
- Mobile apps (iOS/Android LLM apps)
- Desktop applications
- Command-line interfaces (API-based LLMs)
- Self-hosted LLM servers
- Any environment with text input capability

---

## Examples of Topics You Can Create Guides For

### Git & GitHub Topics
- Merge Conflicts & Resolution
- Git Rebase vs Merge
- Git Stash & Uncommitted Changes
- Git Tags & Releases
- Collaborative Workflows
- Code Review Best Practices

### DevOps & Infrastructure
- Docker Containers
- Kubernetes Basics
- CI/CD Pipelines
- GitHub Actions
- Infrastructure as Code

### Programming Concepts
- REST APIs Design
- Microservices Architecture
- Database Transactions
- Caching Strategies
- Authentication & Authorization

### Web Technologies
- React Hooks
- TypeScript Generics
- CSS Grid vs Flexbox
- Web Security
- Performance Optimization

---

## Generated Guide Format Example

When you use the prompt, you get markdown files with this structure:

```markdown
# [Topic]: Complete Guide

## Overview
[Definition & importance]

---

## 1. [Core Concept]
### Visual [Diagram in Mermaid]
### Definition
[Clear explanation]

---

## 2. [Detailed Section]
[Content with examples]

---

## [N]. Quick Cheatsheet
[Commands & syntax]

---

## Real-World Scenarios
[4 practical examples with diagrams]

---

## Interview & Exam Preparation
[Q&A table]

---

## Key Takeaways
[Summary & decision trees]
```

---

## Tips for Best Results

### 1. Be Specific with Topic Names
```
✅ Good:  "Merge Conflicts & How to Resolve Them"
❌ Bad:   "Git"
```

### 2. Include Context if Needed
```
✅ Better: "GitHub Actions for CI/CD in Node.js projects"
❌ Generic: "GitHub Actions"
```

### 3. Combine with Other Prompts
You can use this guide for specific topics, then ask follow-up questions:
```
/createLearningGuide Kubernetes
Then ask: "Add a section on security best practices"
```

### 4. Customize Output
After generation, you can ask to:
- Add more scenarios
- Add more diagrams
- Include more code examples
- Simplify technical language
- Add diagrams for specific sections

---

## Integration with Existing Projects

### In Documentation Folder
```
docs/
  ├── learning-guides/
  │   ├── git-concepts-guide.md
  │   ├── github-workflow-guide.md
  │   └── CREATE_GUIDE_INSTRUCTIONS.md  ← This file
```

### In Team Knowledge Base
- Share this prompt document with your team
- Everyone can generate guides consistently
- Maintain standardized documentation

### In Learning Materials
- Create guides for each course module
- Use for technical documentation
- Generate for training new team members

---

## Troubleshooting

### Prompt Too Long or Truncated?

Split it into multiple messages:
1. Send the structure part first
2. Follow up with formatting & quality guidelines
3. Then specify your topic

### Output Format Not as Expected?

Add specific instructions:
- "Format as a single markdown file"
- "Include diagrams for every major section"
- "Add code examples in Python"
- "Make it suitable for beginners"

### Want a Specific Version or Format?

Ask follow-up questions:
- "Reformat for PDF"
- "Create a summary version"
- "Add more examples"
- "Focus on scenarios section only"

### Can't Copy Text Easily?

The prompt is also available in variations:
1. **Full version** - Everything included (shown here)
2. **Minimal version** - Core structure only (ask in chat)
3. **Detailed version** - With more formatting guidance (ask in chat)

### AI Response Not Matching Your Expectations?

Provide additional context:
- "Make it more technical/beginner-friendly"
- "Include more diagrams"
- "Add security considerations"
- "Focus on [specific aspect]"

---

## Contributing & Improvements

To improve this prompt, consider:

1. **Add more sections** - Template for specific topics
2. **Specify diagram types** - More Mermaid diagram examples
3. **Language customization** - Formal vs casual tone
4. **Audience levels** - Beginner vs advanced
5. **Format variations** - PDF, HTML, Jupyter notebook

---

## Version History

- **v1.0** (Jan 6, 2026) - Initial release
  - 8 standard sections
  - Mermaid diagram support
  - Interview prep included
  - Real-world scenarios

---

## License & Usage

This prompt can be:
- ✅ Used freely in any project
- ✅ Modified and customized
- ✅ Shared with team members
- ✅ Distributed in documentation
- ✅ Used commercially

---

## Related Prompts

Create guides for:
- Specific programming languages
- Framework-specific topics
- Domain-specific concepts
- Interview preparation
- Certification exam prep

---

## Quick Start

**Fastest way to get started:**

1. Copy the **Full Prompt Text** from the section above
2. Open any LLM/AI service (ChatGPT, Claude, Gemini, etc.)
3. Paste the prompt
4. Replace `${the specified technical topic}` with your topic
5. Example: "Create a comprehensive learning guide for 'Merge Conflicts & Resolution' following this standardized structure:..."
6. Submit
7. Get your complete learning guide
8. Save as markdown file
9. Share with your team

**No installation, no configuration, works everywhere.**

---

**Created:** January 6, 2026  
**Status:** Universal Prompt Documentation  
**Compatible with:** All LLMs (ChatGPT, Claude, Gemini, Copilot, Llama, etc.)  
**No Dependencies:** Copy-paste ready, works offline in any format
