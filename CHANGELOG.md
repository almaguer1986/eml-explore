# Changelog

## [0.1.0] — 2026-04-25 — Initial release

E-128 v0 substrate CLI. Six subcommands plus two built-in examples.

### Added

- **`eml-explore witness EXPR`** — full universality witness
  (profile + identification + canonical path + savings + Lean
  status flag). Pretty-printed text or `--json`.
- **`eml-explore analyze EXPR`** — Pfaffian profile only.
- **`eml-explore identify EXPR`** — top N registry matches with
  confidence + domain.
- **`eml-explore class AXES`** — every registry formula in a
  given Pfaffian equivalence class.
- **`eml-explore corpus FILE`** — read one-expression-per-line
  text file, cluster, report top-N class sizes + sample members.
- **`eml-explore example cross-domain`** — built-in demo of the
  Stefan-Boltzmann / perpetuity / kinetic-energy collapse.
- **`eml-explore example witness-walkthrough`** — three-example
  demo of the witness pipeline (textbook sigmoid → canonical;
  Pythagorean → 1; Bessel non-EML).
- Top-level `--json` flag emits machine-readable output for any
  subcommand.

### Tests

- 18 cases in `tests/test_cli.py` covering text + JSON output for
  every subcommand, both built-in examples, error paths, and
  argparse help.
- mypy strict clean.

### Status

Beta. Patent pending. CI matrix mirrors the rest of the eml-*
family (ubuntu/macos/windows × py3.10-3.13).
