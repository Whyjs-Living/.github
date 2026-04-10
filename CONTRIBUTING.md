# Contributing to WhyJS

Thank you for your interest in contributing to WhyJS! This document outlines how to get involved.

## Code of Conduct

All contributors are expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before participating.

## Ways to Contribute

### Reporting Bugs

Before filing a bug, please search existing issues. When filing:
- Use the **Bug Report** issue template
- Include a minimal, reproducible example
- State the WhyJS version (`why --version`) and Node version
- Describe expected vs. actual behaviour

### Proposing Language Changes

WhyJS is a language — design decisions deserve careful thought.

1. Open a **Discussion** first (under the Proposals category)
2. Describe the JS flaw being fixed, your proposed fix, and the semantic change it introduces
3. Explain how `why migrate` would handle the migration
4. Await community + maintainer feedback before opening a PR

### Submitting Pull Requests

1. Fork the relevant repo
2. Create a feature branch: `git checkout -b feat/my-change`
3. Write tests for your change
4. Run the test suite: `npm test`
5. Ensure your code compiles to valid ES2022: `why build`
6. Open a PR against `main` with a clear description

## Commit Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add nullish coalescing fix
fix: correct this-binding in arrow functions
docs: update spec for module semantics
chore: bump dependencies
```

## Development Setup

```bash
git clone https://github.com/Whyjs-Living/whyjs
cd whyjs
npm install
npm test
```

## Questions?

Open a [Discussion](https://github.com/orgs/Whyjs-Living/discussions) or reach out in the community.
