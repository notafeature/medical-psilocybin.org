# medical-psilocybin.org

The hub at the apex of the domain: what the site is, what it covers, and where each area lives. One page, static, served by a Cloudflare Worker with static assets and no code of its own.

The rules site, the tools, the standing rules, and the operations inventory live in the repository `NMMPAB_Rules-Draft-Analysis`; its `ARCHITECTURE.md` and `OPERATIONS.md` govern this project as well. This repository holds only the hub.

| File | What it is |
|---|---|
| `public/index.html` | The page |
| `public/404.html` | The not-found page |
| `public/style.css` | A copy of the rules site's stylesheet, so the hub reads as the same site; refresh it from `docs/style.css` there when that changes |
| `wrangler.jsonc` | The deploy config: Worker name `medical-psilocybin-hub`, custom domains `medical-psilocybin.org` and `www.medical-psilocybin.org` |

Deploy from this folder:

```
npx wrangler@4 deploy --config ./wrangler.jsonc
```

The page carries the visit-counter beacon that every rules page carries, reporting to `count.medical-psilocybin.org`; the counter's `ALLOWED_ORIGINS` names this host. Never add a config for the counter Worker here.

Everything written here follows the writing standard in the rules repository. No em dashes. Nothing here names who compiles it.
