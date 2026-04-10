# WhyJS

> **Layer on top. Fix the core.**

**WhyJS** is a strict superset of JavaScript that compiles to standard **ES2022**. It fixes JavaScript's long-standing design flaws while remaining fully compatible with the existing JS ecosystem. Semantic breaking changes are automatically handled by the `why migrate` tool.

---

## What is WhyJS?

| Property | Detail |
|---|---|
| **Type** | Strict superset of JavaScript |
| **Output** | Standard ES2022 |
| **Migration** | `why migrate` handles semantic breaking changes automatically |
| **Mantra** | Layer on top. Fix the core. |

WhyJS does not fork JavaScript — it extends and corrects it. Every valid JS program is a valid WhyJS program syntactically. WhyJS introduces **semantic fixes** (e.g. better equality, sane type coercion, consistent scoping) that the `why migrate` CLI resolves for existing codebases.

---

## Repositories

| Repo | Description |
|---|---|
| [`whyjs`](https://github.com/Whyjs-Living/whyjs) | Core language compiler & CLI |
| [`why-migrate`](https://github.com/Whyjs-Living/why-migrate) | Migration tool for existing JS codebases |
| [`why-spec`](https://github.com/Whyjs-Living/why-spec) | Language specification & design decisions |
| [`why-playground`](https://github.com/Whyjs-Living/why-playground) | Online playground — try WhyJS in the browser |

---

## Why WhyJS?

JavaScript has well-known design flaws accumulated over 30 years. WhyJS fixes them:

- **No more `==` surprises** — WhyJS enforces strict equality semantics by default
- **Sane `this` binding** — predictable, lexically-scoped `this` everywhere
- **No implicit type coercion** — ops fail loudly instead of silently coercing
- **Module semantics fixed** — clear, consistent import/export behaviour
- **Compiles to ES2022** — runs anywhere modern JS runs, zero runtime overhead

---

## Contributing

WhyJS is open source and community-driven. We welcome:

- Bug reports & feature requests via [Issues](https://github.com/Whyjs-Living/.github/issues)
- Language design proposals in [Discussions](https://github.com/orgs/Whyjs-Living/discussions)
- Pull requests on any repo
- Feedback on the spec

Read our [Contributing Guide](https://github.com/Whyjs-Living/.github/blob/main/CONTRIBUTING.md) to get started.

---

## License

All WhyJS projects are released under the [MIT License](https://github.com/Whyjs-Living/.github/blob/main/LICENSE).
