# VeeCode APIP

**APIP** is an open API Platform built on top of [Kong Gateway](https://github.com/Kong/kong) (OSS).

We maintain a hardened, RHEL-targeted distribution of Kong Gateway, with a simplified release pipeline, a custom SBOM-driven security gate, and a plugins-first extension model.

## What we ship

- A fork of **Kong Gateway** with VeeCode-specific patches and plugins
- Multi-arch (amd64 + arm64) **container images** for RHEL 10, published to Docker Hub as [`veecode/kong`](https://hub.docker.com/r/veecode/kong)
- Signed **RPMs** for RHEL-family distros (RHEL / Rocky / AlmaLinux / CentOS Stream)

Releases follow the `3.10.0-veecode.N` scheme — pinned to the last upstream Kong OSS tag, with the `-veecode.N` suffix tracking our own iterations.

## Repositories

- **kong** — fork of Kong Gateway, with VeeCode patches and the RPM release pipeline
- **docker-kong** — Dockerfiles and the multi-arch image build for `veecode/kong`
- **kong-builder** — local-only build toolchain image for reproducing CI builds on a workstation

## Why APIP

Kong OSS no longer ships tagged releases, and its container images bundle statically-linked native dependencies that container scanners can't see. APIP fills that gap: tagged, reproducible builds, a CycloneDX SBOM scanned at release time, and an extension model that keeps custom features out of merge-conflict territory when we sync upstream.
