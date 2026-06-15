# Contribution [#136]: [Add a way to delete custom providers from configuration]

**Contribution Number:** [1]  
**Student:** [Deep Akbari]  
**Issue:** [https://github.com/alibaba/open-code-review/issues/136](https://github.com/alibaba/open-code-review/issues/136)
**Status:** [Phase II] [Complete]

---

## Why I Chose This Issue

---

## Understanding the Issue

### Problem Description
Currently, open-code-preview supports adding or updating custom providers through:
- ocr config provider (TUI)
- ocr config set custom providers.<name>. <field> <value> (non-interactive)

But, there is no way to delete a coustom provider once it is saved.

To remove, users have to edit ~/.opencodereview/config.json and delete the custom_providers.<name> entry 
by hand. And if deleted provider happens to be the active provider, they also have to manually clear or
change the provider field, otherwise config resolution throws errors.

### Expected Behavior

Add a supported way to delete custom providers (TUI/ UI Layer)

### Current Behavior

Custom providers can only be deleted manually in code.

### Affected Components

[Which parts of the codebase are involved?]

---

## Reproduction Process

### Environment Setup

I forked the repo, followed `CONTRIBUTING.md`'s guidelines to start the dev server, and then created a new branch.

### Steps to Reproduce
1. Forked the repo
2. Cloned locally
3. Followed CONTRIBUTING.md's steps to fully clone the repo and run the dev server
### Reproduction Evidence

- **Commit showing reproduction:** [Link to commit in your fork]
- **Screenshots/logs:** [If applicable]
- **My findings:** [What you discovered during reproduction]

---

## Solution Approach

### Analysis

[Your analysis of the root cause - what's causing the issue?]

### Proposed Solution

[High-level description of your fix approach]

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem]

**Match:** [What similar patterns/solutions exist in the codebase?]

**Plan:** [Step-by-step implementation plan]
1. [Modify file X to do Y]
2. [Add function Z]
3. [Update tests]

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]
