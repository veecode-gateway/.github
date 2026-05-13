# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Content for the **VeeCode APIP** GitHub organization profile page. On GitHub the repo is named `.github` (by convention); GitHub renders `profile/README.md` as the org's public landing page at `github.com/veecode-apip`.

There is no build, no tests, no CI. Edits are pure Markdown + image assets, and become live as soon as they land on `main`.

## Layout

- `profile/README.md` — the org landing page (the only file GitHub renders publicly). The top-level `README.md` is a stub and is **not** what visitors see.
- `assets/` — images referenced from `profile/README.md`. Prefer raw GitHub URLs (`?raw=true`) or absolute URLs for images so they render on the org page.
- `LICENSE` — Apache 2.0.

## Editing notes

- The landing page positions APIP as the **gateway half of the VeeCode Platform**, paired with VeeCode DevPortal (Backstage-based). Keep that framing — APIP is not a standalone product in the messaging.
- The "Kong OSS vs. Kong APIP" comparison table is the load-bearing section. When updating it, keep claims verifiable against the sibling repos (`../kong`, `../docker-kong`, `../apip-parent`) — e.g. the versioning scheme (`3.10.0-veecode.N`), RHEL 10 target, SBOM-based gate, plugins-first policy all map to ADRs in `../docs/adr/`.
- Markdown must be markdownlint-clean (see global rules: blank lines around headings/lists/code fences, language on fenced blocks — use `pre` for non-code).

## Parent repo

This directory is a child repo of `apip-parent/` (filesystem root). See `../CLAUDE.md` for the platform-wide context — release pipeline, versioning scheme, ADRs — that the landing page summarizes.
