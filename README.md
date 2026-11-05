# ninja

Packages the upstream [Ninja](https://github.com/ninja-build/ninja) release binaries as the `ninja` component of [ps2build](https://github.com/ps2build/ps2build). Ninja is not built here.

## Releasing

Push a tag equal to an upstream Ninja release tag, such as `v1.12.1`. The workflow downloads that release's Windows and Linux binaries and the `COPYING` file from the same tag, then publishes:

| Asset | Contents |
|---|---|
| `ninja-<tag>-windows-amd64.zip` | `tools/ninja.exe`, `licenses/ninja/COPYING` |
| `ninja-<tag>-linux-amd64.zip` | `tools/ninja`, `licenses/ninja/COPYING` |

The release fails if `COPYING` cannot be fetched.

## License

Ninja is distributed under Apache-2.0 (`COPYING`, bundled in every archive). The files in this repository are [CC0 1.0](LICENSE).
