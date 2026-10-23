# Jeku CLI — Rust edition

Native command-line client for jeku.ai, version 0.3.22. This distribution contains compiled executables, not the proprietary Rust source.

## Install with npm

```sh
npm install -g @jeku.ai/cli-rust
jeku-rust --version
jeku-rust login
jeku-rust
```

The package bundles the supported executables. Installation requires no Rust compiler and makes no post-install downloads. The installed CLI does not require Node at runtime. The existing `@jeku.ai/cli` package and `jeku` command remain separate.

## Direct download

Download the matching archive from [GitHub Releases](https://github.com/chatroid/jeku-cli-rust-releases/releases), verify it against `SHA256SUMS`, and extract it. Run `./jeku-rust --version`, then move `jeku-rust` to a directory on your PATH.

Supported artifacts:

- `darwin-arm64`: Apple Silicon macOS.
- `linux-arm64`: Linux ARM64 with glibc 2.39 or newer and system C++ libraries.
- `linux-x64`: Linux x86_64 with glibc 2.39 or newer and system C++ libraries. Does not require AVX/AVX2. Execution was validated under baseline x86_64 emulation, not physical x86 hardware.

Windows, Intel macOS, Alpine/musl and Linux GPU support are not part of this release. macOS binaries are not Developer ID signed or notarized.

## Separate account configuration

Rust client state lives in `$XDG_CONFIG_HOME/jeku-cli-rust` or `~/.config/jeku-cli-rust`. Sign in separately; existing Node client settings are not imported. Cloud functionality requires a Jeku account and any applicable service access.

Use `jeku-rust --help` for commands. Gmail and Microsoft live consent flows remain unverified; simulated integration tests passed.

## License

Proprietary software, copyright Chatroid, LLC. See `LICENSE` and `THIRD_PARTY_NOTICES.txt`. Third-party components retain their own licenses.
