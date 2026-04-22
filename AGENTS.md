# Shared Workspace Context — high5-app-guzzle

This repo is part of the High5 workspace. Start by reading the root workspace's `AGENTS.md` (at `../AGENTS.md`) and the files it references; the rules there apply in full.

## What this repo is

A **pinned private fork of Guzzle 3** (`guzzle/guzzle dev-3.8.2-high5 as 3.8.1`), kept alive to support legacy callers in `high5-app` that have not yet been migrated to Guzzle 7. Guzzle 3 itself has been end-of-life since ~2016.

Upstream Guzzle 3 documentation in this repo (`README.md`, `UPGRADING.md`, `CHANGELOG.md`, `docs/`) is preserved from the original project and should be treated as **historical reference only** — any behaviour documented there reflects Guzzle 3's original API, not necessarily the state of this fork.

## Why it still exists

Callers in `high5-app` written against the Guzzle 3 request/response API continue to depend on this package. Migrating them to Guzzle 7 is tracked as a dependency-removal item in [high5-app/TODO.md](../high5-app/TODO.md).

## Rule for working here

Do not add features. This fork exists to stay on life support until the last caller is migrated and the package can be deleted. Any change made here should:

1. Be a security patch or a narrow compatibility fix.
2. Have the rationale recorded in the commit message.

Any broader change belongs in the migration plan for the calling code, not in this repo.
