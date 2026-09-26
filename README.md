# ai-jail Linux ARM64 release mirror

This repository builds the latest [upstream ai-jail](https://github.com/akitaonrails/ai-jail) release for Linux ARM64. It no longer maintains a local source fork.

The single GitHub Actions workflow runs daily at 00:00 UTC (or manually via **Actions → Build upstream ARM64 release → Run workflow**). If the latest upstream release tag already has a release here, it skips the build. Otherwise it checks out the upstream tag, builds `aarch64-unknown-linux-gnu`, and publishes a tarball and SHA-256 checksum to this repository's Releases.

GitHub scheduled workflows require the workflow to be on the default branch and may run later than the scheduled time. The repository must allow GitHub Actions to create releases (Workflow permissions: read and write).
