# FAQ Content — soft-tab.com

> **Status**: Draft — needs owner review
> **Last Updated**: 2026-02-11
> **Source**: Objection handling from `docs/messaging-framework.md`, expanded and mapped to pages.

---

## How FAQs Are Used

FAQs are **not a standalone page**. They appear as collapsible accordion sections embedded in relevant pages. Each question is tagged with the page(s) where it should appear.

This keeps FAQs contextual (visitors see answers relevant to what they're already reading) and supports FAQ schema markup for SEO on each page.

---

## General FAQs

*Appear on: /services, /about*

### How is Soft-TAB different from hiring a freelancer?
Freelancers execute tasks. We own outcomes. That means strategic thinking, architecture decisions, and AI-augmented workflows, not just hours of coding. We also scale our team to match the project, so you're never limited to one person's availability or skill set.

### What technologies do you work with?
Our deepest expertise is in TypeScript, Angular, React, Node.js, and NestJS, but we work across a wide range of stacks including Go, Java, Python, and more. We're stack-flexible and choose the right tool for your problem. See our [full technology list](/services#technologies).

### How much does this cost?
Every project is different, and we don't publish fixed pricing. We offer a free discovery call to understand your needs and provide a clear proposal with scope, timeline, and cost. Engagements range from short-term advisory to multi-month builds.

### Can you work with our existing team?
Absolutely. Team augmentation is one of our core offerings. We embed in your workflow, your tools, and your processes. We've done this with teams of all sizes across many industries.

### What does a typical engagement look like?
It depends on the model. Project delivery has a defined scope and timeline. Fractional engineering is an ongoing partnership. Advisory is flexible hours per week. Every engagement starts with a free discovery call so we can recommend the right structure. See our [engagement models](/services#engagement-models).

### How do you handle communication and updates?
We adapt to your preferences. Some clients want weekly standups. Others prefer async updates via Slack or email. We agree on a communication cadence during kickoff and adjust as needed.

---

## AI-Specific FAQs

*Appear on: /for-ai-adoption, /services*

### What if AI-generated code is low quality?
AI is a tool, not a replacement for engineering judgment. We use AI to accelerate the repetitive parts of development while our senior engineers make every architectural and quality decision. Every output is reviewed, tested, and validated. The result is faster delivery with the same (or higher) quality bar.

### Do you use AI to write all the code?
No. AI assists with drafting, scaffolding, testing, and documentation. Senior engineers design the architecture, make technology decisions, review all output, and own the quality of the final product. AI handles the routine so our engineers can focus on the work that requires judgment and experience.

### Can you train our team to use AI tools?
Yes. We offer hands-on workshops and embedded coaching for engineering teams. The goal is to make your team self-sufficient with AI-augmented workflows, not to create a dependency on us. See our [AI training services](/services).

### Is AI-augmented development safe for production applications?
Yes, when done right. The key is that AI generates suggestions, not decisions. Our engineers evaluate, modify, and test every piece of code before it reaches production. We follow the same code review, testing, and deployment standards as any high-quality engineering team.

---

## Founder-Specific FAQs

*Appear on: /for-founders*

### I'm not technical. How do I know the work is good?
We explain technical decisions in plain language and tie them back to your business goals. You'll see working software every week, not just status reports. And we're always available to walk you through what we built and why.

### How long does it take to build an MVP?
It depends on scope, but most MVPs take 6 to 12 weeks from kickoff to launch. We'll give you a realistic timeline during the scoping phase, not a number designed to win the deal.

### Can you help me figure out what to build?
Yes. Many founders come to us with a vision but not a technical plan. We help translate product ideas into architecture, prioritize features for an initial release, and build a roadmap that balances speed with quality.

### What happens after launch?
That's up to you. We can continue as an ongoing development partner, transition the project to an internal team you hire, or step into a fractional CTO role for ongoing guidance. We'll help you plan the right next step.

---

## Engineering Leader-Specific FAQs

*Appear on: /for-engineering-leaders*

### How fast can you get started?
For most engagements, we can begin within one to two weeks of the discovery call. For urgent situations (project rescue, critical deadlines), we can often move faster.

### How do you ramp up on our codebase?
We've been dropping into large, unfamiliar codebases for years. We read the code, review documentation, ask targeted questions, and start contributing within the first few days. No month-long onboarding processes.

### Will your engineers actually fit into our team culture?
We take culture fit seriously. That's why we include a fit assessment before every engagement. If we're not the right match for your team's working style, we'll say so upfront.

### What if the project is already in trouble?
That's one of our specialties. We've rescued projects with runaway tech debt, missed deadlines, and teams that lost momentum. We assess the situation, create a recovery plan, and start executing. See our [rescue and modernization services](/services).

---

## Implementation Notes

### FAQ Schema (SEO)
Each page with an FAQ section should include `FAQPage` structured data markup. This helps Google display rich results (expandable Q&A) in search.

### Design
- Collapsible accordion format (click to expand)
- Section headline: "Frequently asked questions" or "Common questions"
- Place near the bottom of each page, above the final CTA
- Keep answers concise. Link to other pages for details rather than explaining everything inline.

### Maintenance
- This document is the single source of truth for FAQ content
- Update answers here first, then propagate to the built pages
- Review quarterly for accuracy (especially pricing language and technology list)
