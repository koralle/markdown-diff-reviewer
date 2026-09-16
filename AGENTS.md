# markdown-diff-reviewer

Reviews Markdown diffs between git revisions at AST level (mdast),
classifying changes as visible / source-only / cosmetic.

- `mdr` — CLI binary (`crates/mdr`)
- Desktop app built on GPUI is planned (macOS-first)

## Guardrails

- `mise run setup` — install dev tools and enable git hooks (lefthook)
- `mise run check` — fmt check + Clippy (runs on pre-commit)
- `mise run test` — nextest (runs on pre-push, with `mise run deny`)
- `mise run -j 1 ci` — everything CI runs, locally
- Workspace lints deny `unwrap`/`expect`/`panic!`/`todo!`/`unimplemented!`/`dbg!`

When working on Rust:

- Use actionbook/rust-skills to reason about ownership, design,
  domain constraints, and compiler errors.
- Use leonardomso/rust-skills for concrete idiomatic Rust guidance.
- Repository-specific rules always take precedence.
- Do not apply generic crate/library recommendations mechanically.
