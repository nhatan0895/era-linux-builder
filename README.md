# ERA Linux Builder

Public GitHub Actions builder for ERA PI Linux AppImage.

This repository intentionally contains no ERA source code. Its workflow checks out the private `nhatan0895/era` repository using a read-only token, builds the Linux x64 desktop bundle, and uploads stable assets to `nhatan0895/era-releases`.

## Required secrets

- `ERA_SOURCE_TOKEN`: fine-grained PAT with read-only `Contents` access to `nhatan0895/era`.
- `RELEASES_REPO_TOKEN`: fine-grained PAT with read/write `Contents` access to `nhatan0895/era-releases`.

## Run

Actions -> Release ERA PI Linux -> Run workflow

Inputs:
- `tag`: release tag, for example `v0.1.17`
- `ref`: source ref in `nhatan0895/era`, for example `otna/cloud-mvp`
