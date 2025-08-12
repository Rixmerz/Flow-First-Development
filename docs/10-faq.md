# Frequently Asked Questions (FAQ)

Common questions and answers about Flow First Development methodology.

## 🎯 General Methodology

### Q: How is FFD different from Agile/Scrum?
**A**: While Agile focuses on iterative development with flexible scope, FFD emphasizes **strict sequential order** following user flow. Agile might build features in parallel sprints; FFD builds them in the exact order users will experience them. They can be combined—you can do FFD within Agile sprints.

### Q: What if my user flow has multiple parallel paths?
**A**: Handle parallel paths hierarchically:
1. Identify the **primary path** (most common user journey)
2. Complete primary path fully
3. Build secondary paths in order of business importance
4. Ensure each path has clear entry/exit points to main flow

### Q: Can FFD work with microservices architecture?
**A**: Yes, but requires coordination:
- Each microservice should follow FFD within its domain
- Cross-service dependencies must be mapped in flow order
- API contracts should be established before dependent services start
- Integration testing should follow the user flow sequence

---

## 🔧 Implementation Challenges

### Q: What if a dependency is blocked or delayed?
**A**: FFD's strength is making blockers visible early:
1. **Identify the blocker** immediately (don't work around it)
2. **Escalate or resolve** before continuing
3. **Use the time** to polish current milestone or plan ahead
4. **Never skip ahead** to later milestones—this breaks the methodology

### Q: How do I handle urgent bug fixes in production?
**A**: Production issues always take priority:
1. **Fix critical production issues** immediately
2. **Assess impact** on current milestone
3. **Adjust timeline** realistically  
4. **Continue FFD flow** once stable
5. **Learn and prevent** similar issues in future milestones

### Q: What about refactoring and technical debt?
**A**: Technical debt should be addressed within the flow:
- **Immediate refactoring**: Do it within current milestone
- **Major refactoring**: Plan as its own milestone if it blocks user flow
- **Nice-to-have refactoring**: Schedule after user flow is complete
- **Never refactor** speculatively—only when it blocks progress

---

## 👥 Team Management

### Q: How do I convince stakeholders to follow FFD?
**A**: Focus on business benefits:
- **Show early progress**: Working features every milestone
- **Reduce risk**: Dependencies clear, no surprise blockers
- **Enable early testing**: Real user feedback sooner
- **Provide predictability**: Clear "what's next" always visible
- **Use examples**: Share case studies from similar projects

### Q: What if developers want to work on "more interesting" features first?
**A**: Address through team alignment:
- **Explain the why**: User value delivery and dependency management
- **Rotate responsibilities**: Everyone gets interesting work across milestones
- **Highlight challenges**: Even "simple" features have complex edge cases
- **Show progress**: Satisfaction from completing full user journeys
- **Set expectations**: Professional growth comes from user impact, not just technical complexity

### Q: How do I manage a team that's used to parallel development?
**A**: Gradual transition works best:
1. **Start with pilot project** using FFD
2. **Demonstrate benefits** with clear metrics
3. **Train on dependency mapping** skills
4. **Establish new rituals** around milestone validation
5. **Celebrate sequential wins** to build confidence

---

## 🤖 AI and Automation

### Q: How does FFD work with AI-assisted development?
**A**: FFD is ideal for AI tools:
- **Clear context**: AI knows exactly what to build next
- **Sequential prompts**: Each milestone provides context for the next
- **Validation checkpoints**: AI output validated before proceeding
- **Incremental complexity**: AI handles simple tasks first, builds complexity
- **See our [AI Integration Guide](../guides/integrating-ai.md)** for details

### Q: Can AI tools help with dependency mapping?
**A**: Yes, AI can assist but human oversight is crucial:
- **Flow analysis**: AI can suggest user journey steps
- **Dependency detection**: AI can identify technical dependencies
- **Risk assessment**: AI can flag potential blockers
- **Validation needed**: Human expertise required for business logic and edge cases

### Q: What about automated testing in FFD?
**A**: Testing follows the same sequential principle:
- **Test current milestone** thoroughly before next milestone
- **Build test suite incrementally** following user flow
- **Integration tests** mirror user journey sequence
- **Automated regression** runs on completed milestones only

---

## 📊 Project Types and Scaling

### Q: Does FFD work for large enterprise projects?
**A**: Yes, with adaptations:
- **Hierarchical flows**: Break into major flows, then detailed milestones
- **Multiple teams**: Each team follows FFD within their domain
- **Cross-team coordination**: Dependencies mapped across teams
- **Extended timelines**: Milestones may be 2-4 weeks instead of 1-2 weeks

### Q: What about research and experimental projects?
**A**: FFD adapts to uncertainty:
- **Research milestones**: Each milestone tests a hypothesis
- **Proof-of-concept flow**: User journey through research questions
- **Pivot-friendly**: Clear stopping points to reassess direction
- **Evidence-based**: Each milestone provides data for next decision

### Q: Can FFD work for mobile app development?
**A**: Perfectly suited for mobile:
- **Platform coordination**: iOS/Android teams work on same milestone
- **API dependencies**: Backend built in sync with mobile needs
- **App store flow**: Submission process becomes final milestone
- **See [Case Study 4](./09-case-studies.md#case-study-4-mobile-app-with-backend-api)** for example

---

## 🎨 Design and UX

### Q: How do I handle design and user research in FFD?
**A**: Design follows the same flow principles:
- **Design milestone 1** before building milestone 1
- **User research** informs current milestone, not future ones
- **Iterate design** based on built milestone feedback
- **Don't over-design** future milestones—they may change

### Q: What about design systems and component libraries?
**A**: Build components as needed:
- **Create components** when milestone requires them
- **Abstract after usage** not before
- **Evolve design system** through actual implementation
- **Avoid pre-building** components for future milestones

---

## 🔄 Process Integration

### Q: How does FFD integrate with existing project management tools?
**A**: FFD works with any PM tool:
- **Jira**: Each milestone becomes an Epic, features become Stories
- **Trello**: Boards for each milestone, cards for tasks
- **Linear**: Milestones as Projects, sequential issues
- **GitHub Projects**: Milestone-based project boards

### Q: What about continuous integration/deployment?
**A**: CI/CD enhances FFD:
- **Deploy each milestone** to staging automatically
- **Production releases** follow milestone completion
- **Feature flags** can hide incomplete milestones
- **Rollback capability** protects completed milestones

### Q: How do I measure success with FFD?
**A**: Key metrics to track:
- **Milestone completion rate**: % of milestones delivered on time
- **User acceptance rate**: % of milestones accepted without major changes  
- **Dependency prediction accuracy**: How well you identified blockers
- **Time to first user value**: How quickly users can use basic functionality
- **Rework percentage**: How much previous work needs changing

---

## 🚨 Common Pitfalls

### Q: What's the biggest mistake teams make with FFD?
**A**: **Skipping ahead when blocked**. Teams often want to "make progress" on later milestones when current ones are stuck. This breaks FFD and creates the same problems traditional development has.

### Q: How do I avoid scope creep during milestones?
**A**: Strict milestone definition:
- **Write clear acceptance criteria** before starting
- **Stakeholder sign-off** on milestone scope
- **Document scope changes** and their impact on timeline  
- **Defer enhancements** to later milestones or phases

### Q: What if I didn't identify all dependencies upfront?
**A**: It's normal to discover dependencies:
1. **Stop current work** when dependency discovered
2. **Re-evaluate milestone** scope and timeline
3. **Address dependency** before continuing
4. **Update documentation** for future reference
5. **Learn and improve** dependency mapping for next project

---

## 🔮 Advanced Topics

### Q: How does FFD handle technical debt and refactoring?
**A**: Address debt strategically:
- **Blocking debt**: Fix immediately if it prevents milestone progress
- **Quality debt**: Address during milestone if time allows
- **Future debt**: Document but don't fix until it actually blocks progress
- **Architectural debt**: Plan dedicated milestone if it affects user flow

### Q: Can FFD work with outsourced or offshore teams?
**A**: Yes, clear sequential structure helps remote coordination:
- **Clear handoffs**: Previous milestone complete before next starts
- **Reduced coordination**: Less parallel work means fewer sync issues
- **Obvious blockers**: Dependencies are explicit and visible
- **Progress visibility**: Stakeholders can see concrete advancement

### Q: How do I adapt FFD for maintenance and support projects?
**A**: Apply flow thinking to support:
- **User report flow**: Issue → Investigation → Fix → Deployment → Verification
- **Feature request flow**: Request → Analysis → Design → Implementation → Release
- **Bug triage flow**: Report → Reproduce → Prioritize → Assign → Fix

---

## 💡 Getting Started

### Q: What's the smallest way to try FFD?
**A**: Start with a single feature:
1. **Map the user flow** for that feature (3-5 steps)
2. **Define 2-3 milestones** within that feature
3. **Build sequentially** with validation between milestones
4. **Measure the difference** in predictability and user satisfaction

### Q: Where can I get help implementing FFD?
**A**: Multiple resources available:
- **[Getting Started Guide](../guides/getting-started.md)**: Step-by-step implementation
- **[Case Studies](./09-case-studies.md)**: Real examples to learn from
- **[Templates](../templates/)**: Ready-to-use project templates
- **Community**: Share experiences and get help from other FFD practitioners

---

## 📚 Additional Resources

- **[Overview](./00-overview.md)**: Repository guide and navigation
- **[Principles](./02-principles.md)**: Core FFD concepts
- **[Implementation](./04-implementation.md)**: Detailed how-to guide
- **[Case Studies](./09-case-studies.md)**: Real-world examples
- **[Templates](../templates/)**: Project management tools