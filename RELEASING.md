# Publishing to crates.io

1. Update the version and supported-backend information in README.md.
2. Run CI and the Windows D3D12 and macOS VideoToolbox tests with the repository FFmpeg SDK.
3. Inspect the archive with `cargo package --list` and verify the default-feature package with `cargo publish --locked --dry-run`.
4. Authenticate using `cargo login` on a trusted machine and run `cargo publish --locked`.
5. Verify the version in the registry before creating a matching Git tag.

The package distributes library source. Native feature validation requires the platform FFmpeg SDK. The SDK and its notices are prepared separately.
