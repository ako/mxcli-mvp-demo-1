# MxcliDemo1

A Mendix app developed with [mxcli](https://mxcli.org), bootstrapped from the
mxcli.org empty-repo prompt.

## What it is

**A webshop logistics management app** (the user's words). It is used to keep
track of the physical side of a webshop: what products are sold, where stock is
held, which orders are waiting to be fulfilled, and how they are shipped.

- **One app**, not a solution.
- **No security** — project security level is `Off`; there are no user roles to
  design for.
- Theme: `signal`. Mendix version: **11.13.0**.

The requirements, grouped into deliverable slices, are in
[`docs/brain/plan/`](docs/brain/plan/). Progress is computed from the model:

```bash
./mxcli brain plan -p MxcliDemo1.mpr
```

## Working on it

```bash
./mxcli run --local -p MxcliDemo1.mpr --watch     # app at http://localhost:8080/
./mxcli exec change.mdl -p MxcliDemo1.mpr         # apply an MDL change
```

A fresh Claude Code session runs `.claude/bootstrap-mxcli.sh` on start, which
fetches `mxcli` and provisions MxBuild, the runtime and the database. See
`CLAUDE.md` for the gates every change goes through, and `FINDINGS.md` for
what surprised us along the way.
