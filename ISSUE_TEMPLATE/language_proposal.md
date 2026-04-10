---
name: Language Proposal
about: Propose a fix, change, or new feature to the WhyJS language
title: '[PROPOSAL] '
labels: proposal, language-design
assignees: ''
---

> **Before submitting:** Please open a [Discussion](https://github.com/orgs/Whyjs-Living/discussions) first to validate your idea with the community. This template is for formalised proposals after initial discussion.

## Summary

One-sentence summary of the proposed change.

## The JavaScript Problem

What specific JS design flaw or limitation does this address?

```js
// Example of the problematic JS behaviour
```

## Proposed WhyJS Behaviour

How should WhyJS handle this?

```whyjs
// Example of the fixed WhyJS behaviour
```

## Compiled ES2022 Output

What should `why build` emit for the above?

```js
// The ES2022 output
```

## Migration Path (`why migrate`)

How should `why migrate` automatically handle existing codebases?

- [ ] Non-breaking (no migration needed)
- [ ] Automatically migratable (describe the transform below)
- [ ] Requires manual intervention (explain below)

**Migration transform description:**

## Alternatives Considered

Other approaches that were considered and why they were rejected.

## Discussion Link

Link to the prior Discussion thread: #
