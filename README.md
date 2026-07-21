# peko-llvm-dist

Prebuilt LLVM 18 distributions for the Peko toolchain. The `peko-tools` build
fetches the archive matching its target from the release attached to this
repository; `peko setup` installs the same payload for end users.

One archive per host target:

| Asset | Target |
|---|---|
| `llvm-18-aarch64-macos.tar.xz` | macOS arm64 |
| `llvm-18-x86_64-macos.tar.xz` | macOS x86_64 |
| `llvm-18-aarch64-linux.tar.xz` | Linux arm64 |
| `llvm-18-x86_64-linux.tar.xz` | Linux x86_64 |
| `llvm-18-x86_64-windows.zip` | Windows x86_64 |

Each archive extracts to a prefix root containing `bin/`, `lib/`, `include/`,
and `LICENSE.TXT`.

## License

This repository redistributes **LLVM**, which is licensed under the
**Apache License, Version 2.0, with LLVM Exceptions**. It is redistributed
unmodified. The full license text is included in every archive as
`LICENSE.TXT`, and a copy is kept here as [LICENSE.TXT](LICENSE.TXT).

Upstream: <https://github.com/llvm/llvm-project/releases/tag/llvmorg-18.1.8>

The LLVM exception waives Apache-2.0 sections 4(a), 4(b), and 4(d) for portions
of LLVM embedded into compiler output, which is why programs compiled with Peko
do not have to carry Apache-2.0 notices for the runtime pieces the compiler
embeds in them.

Nothing in this repository is Peko-authored code. Peko's own toolchain is
licensed under the MIT License and lives at
[official-peko/peko-tools](https://github.com/official-peko/peko-tools).
