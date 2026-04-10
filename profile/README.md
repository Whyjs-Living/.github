# WhyJS

**The question that fixes JavaScript.**

WhyJS is a strict superset of JavaScript that compiles to standard **ES2022**. It fixes JavaScript's most notorious design flaws — nil confusion, loose equality, implicit globals, silent NaN propagation, unhandled async mistakes, and more — without breaking ecosystem compatibility. Rename any `.js` file to `.why` and it compiles. New safety features are additions, never replacements.

---

## What WhyJS Fixes

| # | JavaScript Problem | WhyJS Fix |
|---|---|---|
| 1 | `null` vs `undefined` confusion | Unified as `nil`. Both compile to `undefined`. |
| 2 | `let`/`const`/`var` ambiguity | `val` = immutable (default), `let` = mutable, `var` emits a warning. |
| 3 | `==` coercion bugs | `==` is a **parse error**. Only `===` exists. |
| 4 | `number` is one type | `int`, `float`, `decimal` as compile-time annotations. Hard types in Wasm. |
| 5 | `NaN !== NaN` footgun | `NaN` is a `NumberError` in the type system. Silent propagation is prevented. |
| 6 | `.sort()` on numbers | Compiler warns and auto-emits `(a, b) => a - b` comparator. |
| 7 | `parseInt` without radix | `parseInt` without a radix is a **compile-time error**. |
| 8 | CommonJS / ESM confusion | ESM-only. `require` emits a warning; `why migrate` rewrites to `import`. |
| 9 | Unhandled promise rejections | Floating `async` call without `await`, `.catch()`, or assignment is a **compile-time error** (E004). |

---

## Features

- **Nil safety** — `nil` unifies `null` and `undefined`. Optional types with `T?`, flow-sensitive narrowing, non-nullable by default.
- **Actor model** — Built-in structured concurrency with Web Worker message-passing RPC. `pub` methods, `@MainActor`, `Actor.spawn`, `Actor.all`.
- **WebAssembly AOT** — `@wasm` marks typed functions for sandboxed high-performance execution in a Worker.
- **Tree-shaken stdlib** — Import only what you use from `@std/*` / `@why/std/*`. Collections, strings, async, numbers, validation, logging, benchmarking.
- **Integrated toolchain** — One CLI for build, migrate, format, lint, test, benchmark, LSP, and self-hosting analysis.
- **LSP + VS Code** — Real-time diagnostics, hover types, completions, code actions, and go-to-definition.
- **Zero-config migration** — `why migrate ./src` converts `null`/`undefined` → `nil`, `==` → `===`, `var` → `val`/`let`, and more.

---

## CLI

| Command | Description |
|---|---|
| `why build` | Compile `.why` to ES2022 JavaScript |
| `why migrate` | Convert `.js` files to `.why` semantics |
| `why test` | Run Vitest in the given directory |
| `why dev` | Watch mode — recompile on change |
| `why fmt` | Opinionated formatter (2 spaces, single quotes, semicolons) |
| `why lint` | Lint and typecheck all `.why` files |
| `why bench` | Run benchmarks with statistical output |
| `why lsp` | Start the Language Server Protocol (stdio) |
| `why selfhost` | Analyze TypeScript for WhyJS self-hosting gaps |

---

## Repositories

| Repo | Description |
|---|---|
| [`whyjs`](https://github.com/Whyjs-Living/whyjs) | Core language, compiler, CLI, LSP, stdlib, tests, and docs |
| [`.github`](https://github.com/Whyjs-Living/.github) | Organization profile, community health files, and shared metadata |

---

## Current Status

WhyJS **v0.1.0** ships a complete compiler/toolchain with:

- Lexer, recursive-descent parser, type checker, and ES2022 codegen
- Full diagnostic system (30+ error codes, 10 lint rules)
- Actor model runtime, `@wasm` stub generation, and `@std/*` stdlib
- CLI with build, migrate, fmt, lint, bench, lsp, dev, test, selfhost
- VS Code extension with syntax highlighting and LSP integration
- Vitest test suite with e2e and CLI tests

See the [roadmap](https://github.com/Whyjs-Living/whyjs#roadmap) for what's next: real Wasm binary output, generics, full JS superset coverage, esbuild integration, and self-hosting.

---

## Contributing

Contributions, issues, and language feedback are welcome through the [`whyjs`](https://github.com/Whyjs-Living/whyjs) repository.

- Bug reports & feature requests via [Issues](https://github.com/Whyjs-Living/whyjs/issues)
- Language design proposals in [Discussions](https://github.com/orgs/Whyjs-Living/discussions)
- Pull requests on any repo

See [CONTRIBUTING.md](https://github.com/Whyjs-Living/whyjs/blob/main/CONTRIBUTING.md) to get started.

---

## License

MIT — see [LICENSE](https://github.com/Whyjs-Living/whyjs/blob/main/LICENSE) for details.
