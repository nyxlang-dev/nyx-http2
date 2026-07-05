# nyx-http2 — Retired: HTTP/2 is built into the Nyx language

**This repo is retired (2026-07-05).** HTTP/2 support was never a separate
library — it lives in the Nyx language core:

- `std/http2` — server framework (`h2_serve`, frame API)
- `runtime/http2.c` — HPACK encoder/decoder + frame parser

**Where to go:**

- Language repo: https://github.com/nyxlang-dev/nyx
- Runnable example: [`examples/http2-server.nx`](https://github.com/nyxlang-dev/nyx/blob/main/examples/http2-server.nx) (copy kept here in `examples/`)
- API reference: [`docs/HTTP2.md`](https://github.com/nyxlang-dev/nyx/blob/main/docs/HTTP2.md)

```bash
# With the Nyx toolchain installed (curl -sSf https://nyxlang.com/install.sh | sh):
nyx run examples/http2-server.nx    # h2c server on :3004
curl --http2-prior-knowledge http://localhost:3004/
```
