# Contribution [#4238]: [Add support for Copilot Spaces]

**Contribution Number:** [3]  
**Student:** [Deep Akbari]  
**Issue:** [https://github.com/GoogleCloudPlatform/khi/issues/827](https://github.com/google/go-github/issues/4238)

## Why I Chose This Issue
I chose this issue because this would be my third issue working with Go, and this issue was super fun to work with. I was basically adding Github's new Copilot Spaces feature within go's github api. I had fun adding the new endpoints and tests, and communicating with the maintainers. 
fyi: the scope of the current issue is pretty big, which would take a few more PRs to cover, so I might keep working within the same issue for my next contribution, but different PR.  


---

## Understanding the Issue

### Problem Description
go-github is a go based github api access with simplified methods (you don't have to call the whole endpoint with github's official url; go-github makes it simple to call github api easily, and keeps the code readable). Recently, Github added a new feature called Copilot Spaces that lets owners create a space within their repo where the context of the repo (docs, codebase, etc) is stored uniformly and people can chat to it and ask questions. That feature was not implemented within go-github yet, and this issue basically covers that. 

### Expected Behavior

After this PR, the users can call 5 basic endpoints to copilot spaces (List total spaces, Get a space, create a space, update a space, and delete a space)

### Current Behavior

The repo does not have defined endpoints for copilot spaces.

### Affected Components

`copilot.go` : Added the endpoints here, as this file is associated with all the copilot related structs and methods
`copilot_test.go` : Added tests with edgecases for the same methods

---

## Reproduction Process
It was not a bug, but an enhancement/feature. I added the feature rather than removing anything. 

### Environment Setup

I forked the repo, followed `CONTRIBUTING.md`'s guidelines to start the dev server, which involved cloning locally, and then running some scripts before commits. 

### Steps to Reproduce
1. Forked the repo
2. Cloned locally
3. Followed CONTRIBUTING.md's steps to fully clone the repo.


### Reproduction Evidence

- **Commit showing reproduction:** [Link to commit in your fork]
I don't have a commit to show "reproduction", but have commits to show one-by-one enhancements. Here: [Commit Link](https://github.com/google/go-github/pull/4379/changes/6dbc3f4ec0a62509ab49552654de33f46d50abe6) 

- **Screenshots/logs:** [If applicable]
not applicable.


- **My findings:** [What you discovered during reproduction]
I mainly learned a lot about defining CRUD endpoints, communicating my thought process while I wrote methods. 

---

## Solution Approach

### Analysis

I used AI to first understand the codebase. It was not really as complex as my last PR. This codebase was easy to navigate and I used AI to refine my understanding and scope down the files that I would be working with, and then I read those files. 

### Proposed Solution

After understanding, I commented my thought process and a few questions to the maintainer. He communicated with an approval and I started to work.
I started by first defining 5 basic methods for the first PR. I would define more endpoints in the coming PRs. 

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:**
go-github currently does not support Copilot Spaces

**Match:** 
I added five simple CRUD endpoints that followed codebase standards and Go tests to safety check.

**Plan:** 
1. Add the five methods, with a test method for each method.
2. Commit each method + test 
3. Create a PR
4. Work on next phase post approval

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- `github/copilot_test.go` — added 5 unit tests `TestCopilotService_ListOrganizationCopilotSpaces`, `TestCopilotService_GetOrganizationCopilotSpace`, `TestCopilotService_CreateOrganizationCopilotSpace`, `TestCopilotService_UpdateOrganizationCopilotSpace`, `TestCopilotService_DeleteOrganizationCopilotSpace`


### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

I called the endpoints manually to check the status code and then relied on pre-built check shell files. 

---

## Implementation Notes

### Week [1] Progress
 - Fortunately, I was not too busy this week and the maintainer was always quick to get back. I finished this PR in under a week.


### Code Changes

- **Files modified:** 2 total files changed: [ 
    1. `github/copilot.go`
    2. `github/copilot_test.go`
]


- **Key commits:** [
    [Initial Commit](https://github.com/google/go-github/pull/4379/changes/6dbc3f4ec0a62509ab49552654de33f46d50abe6)
    [First Commit](https://github.com/google/go-github/pull/4379/changes/c2207db4bf6aafb457e3ba227c045cf9d313a7b0)
    [Second Commit](https://github.com/google/go-github/pull/4379/changes/bfeaa035fcc68bbdfab1cb31fd8031983556d32d)
    [Third Commit](https://github.com/google/go-github/pull/4379/changes/377b890ab4f35a507ef2ccbb2cec8327533ebd2f)
    [Fourth Commit](https://github.com/google/go-github/pull/4379/changes/960c32f12d328ddf87b833b99b7a9f5ca9863547)
    [Fifth Commit](https://github.com/google/go-github/pull/4379/changes/80a149ba2fdd4a0edf0ea64049fb146517b2e388)
]
- **Approach decisions:** 
I first understood the codebase, found the relevant files that are going to be affected and looked for files that depended on the change. After that, I scoped out the issue and presented my approach to maintainer. After approval, I started on implementing the endpoints. After that, I communicated with the maintainer and incorporated feedback.

---

## Pull Request

**PR Link:** [go-github/pull/4379](https://github.com/google/go-github/pull/4379/)

**PR Description:** 
Adds support for the core organization Copilot Spaces endpoints:

List organization Copilot Spaces
Get an organization Copilot Space
Create an organization Copilot Space
Update an organization Copilot Space
Delete an organization Copilot Space
Solves #4238 partially.

**Maintainer Feedback:**
- [07/13/26]: The maintainer found out I had forgot to run one of the scripts before creating the PR, which resulted in a workflow fail. 
- [07/13/26]: After fixing the lint and generate errors, the maintainer pointed out some items in the struct that I had set optional. They were set as required as per github's official api so I set them as required too

**Status:** [Awaiting review]

---

## Learnings & Reflections
I learned a lot about working with not known codebases, Golang practices, defining CRUD endpoints


### Technical Skills Gained

More knowledge about Go, writing unit tests, and performing http requests.

### Challenges Overcome

The hard part was writing the unit tests. The method params took a really big struct, so i had to define a model one for different edge cases.

### What I'd Do Differently Next Time

make sure to review the contributing.md again before creating a PR.

---

## Resources Used

- [Holy Grail](claude.ai)
