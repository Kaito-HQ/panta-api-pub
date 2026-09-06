# Panta API docs

Public Mintlify documentation for the Panta Markets API: what you can build, which endpoints to call, and how signing stays on the client.

## Local preview

```bash
npx mintlify dev
```

Opens at the URL Mintlify prints (usually `http://localhost:3000`).

## Layout

| Path | Contents |
| --- | --- |
| `docs.json` | Site config, branding, navigation, API playground |
| `index.mdx`, `quickstart.mdx`, `guides/` | Product + integration guides |
| `api-reference/` | One page per HTTP endpoint |
| `logo/`, `favicon.svg` | Brand assets |

## Source of truth

Endpoint contracts are adapted from `panta-dev` (`docs/external/` and the live Django routes). Prefer the running API when docs and code diverge.

Auth note: authenticated routes accept **either** `X-Api-Key` or signup JWT. Live hosts accept `pk_test_` and `pk_live_`; test hosts accept `pk_test_` only.

## Publish

Connect this repo to [Mintlify](https://mintlify.com) (GitHub app). Pushes to `main` deploy the site.
