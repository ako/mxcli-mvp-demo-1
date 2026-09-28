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

## 2026-09-28 — quality baseline (blank template, before any of our work)

Booted with `./mxcli run --local -p MxcliDemo1.mpr`: HTTP 200 at
http://localhost:8080/ after ~70 s (cold).

- `mxcli lint`: **8 issues — 0 errors, 0 warnings, 8 info** (all in
  `MyFirstModule`: missing documentation, `MyFirstLogic` unprefixed and unused,
  a role-mapping hint).
- `mxcli report`: overall **99/100**. Security 99 · Quality 95 ·
  Architecture 100 · Performance 100 · Naming 99 · Design 100 · Other 99.

These are what the template ships with; later scores compare against them.
- `New` is a reserved word as an enumeration value (CE7247, caught by
  `mxcli check --references` as MDL010). The first order status is `Received`.
