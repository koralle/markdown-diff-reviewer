# markdown-diff-reviewer

Reviews Markdown diffs between git revisions at AST level (mdast) and
classifies each change as visible, source-only, or cosmetic.

Early development. Planned components:

- `mdr` — CLI binary
- Desktop app built on GPUI (macOS-first)

## Development

Requires [mise](https://mise.jdx.dev/). The Rust toolchain is pinned in
`rust-toolchain.toml`.

```sh
mise run setup    # install dev tools + git hooks (lefthook)
mise run -j 1 ci  # run all CI checks locally
```

## License

Licensed under either of [Apache License, Version 2.0](LICENSE-APACHE)
or [MIT license](LICENSE-MIT) at your option.
