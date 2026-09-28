# Findings

Anything surprising or broken while building MxcliDemo1, appended as work proceeds.

Environment: Mendix 11.13.0 (MxBuild was already cached in `~/.mxcli/mxbuild/`),
mxcli `nightly-20260927-95091765`, Claude Code on the web (Linux container).

## 2026-09-28 — bootstrap

- `mxcli` was already on `PATH` (`/usr/local/bin/mxcli`) as well as downloaded
  to `./mxcli` by the seed prompt; both report the same nightly.
- The blank 11.13.0 app already ships with project security `Off`, which is what
  was asked for — no change needed. (Verified with `show project security`.)
- Moving the project up from `MxcliDemo1/` overwrote the repo's placeholder
  `README.md` and the seed `.gitignore` (which only ignored `/mxcli`); the
  generated `.gitignore` already ignores `mxcli`, so nothing was lost.
- `mxcli brain` queue lives in `.mxcli/` (git-ignored): captures must be
  promoted before committing, or the plan never reaches git.
