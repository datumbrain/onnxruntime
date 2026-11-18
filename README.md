# onnxruntime binaries

Prebuilt ONNX Runtime shared libraries that Picono ships, kept here because
`github.com/microsoft/onnxruntime` and its release downloads have returned 404
since 17 November 2026.

These are unmodified Microsoft builds, stored with Git LFS:

| Path | Version | Platform | Taken from |
| --- | --- | --- | --- |
| `1.31.1/osx-arm64/libonnxruntime.dylib` | 1.31.1 | macOS, Apple Silicon | `onnxruntime-osx-arm64-1.31.1.tgz` (official GitHub release), `lib/libonnxruntime.1.31.1.dylib` |
| `1.23.2/osx-x86_64/libonnxruntime.dylib` | 1.23.2 | macOS, Intel | `onnxruntime-osx-x86_64-1.23.2.tgz` (official GitHub release), `lib/libonnxruntime.1.23.2.dylib` |
| `1.31.1/linux-x64/libonnxruntime.so` | 1.31.1 | Linux x86-64 | NuGet `Microsoft.ML.OnnxRuntime` 1.31.1, `runtimes/linux-x64/native/` (byte-identical to the GitHub release) |
| `1.31.1/linux-aarch64/libonnxruntime.so` | 1.31.1 | Linux arm64 | NuGet `Microsoft.ML.OnnxRuntime` 1.31.1, `runtimes/linux-arm64/native/` (byte-identical to the GitHub release) |

`SHA256SUMS` lists each file's checksum. They are the same sums pinned in
Picono's `scripts/fetch-resources.sh`, so check them after downloading:

```sh
shasum -a 256 -c SHA256SUMS
```

ONNX Runtime is MIT licensed, copyright Microsoft Corporation. See `LICENSE`
and `ThirdPartyNotices.txt`.
