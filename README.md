# onerecord-xlsx-tools

Tooling for converting IATA OneRecord working-draft xlsx fixtures to JSON, for use by [`@flaks/onerecord`](https://github.com/tjo099/onerecord-mapper).

This repo exists as a sibling to the main library so that the `xlsx` (SheetJS) dependency — which carries Prototype Pollution and ReDoS advisories — does not appear in the main library's runtime or dev dependency tree.

## Usage

```bash
bun install
bun run convert:fsu
```

Output is written to `xfsu-status-codes.json`. The pinned `sha256:` blob hash in the output is the canonical drift-detection anchor.

## Scope

Currently:
- `convert-iata-xlsx.ts` — fetches and parses the IATA-Cargo XFSU Status Codes xlsx.

Future tools (per upstream IATA-Cargo working-draft activity) will be added to this repo as separate scripts.

## License

Apache-2.0.
