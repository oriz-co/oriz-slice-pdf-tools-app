# oriz-pdf-tools

> 📄 **PDF Tools** — Merge, split, compress, sign, redact, OCR. Never uploaded.
>
> Live site: [https://pdf.oriz.in](https://pdf.oriz.in)

Free, browser-based PDF toolkit. 30+ tools that run 100% client-side using
`pdf-lib`, `pdfjs-dist`, and `tesseract.js` — your files never leave your device.

Part of the [oriz](https://github.com/chirag127/oriz) family of static sites by
[Chirag Singhal](https://oriz.in/about/). Shares the
[`@chirag127/oriz-ui`](https://github.com/chirag127/oriz-ui) design system with
nine sibling sites.

## Develop

```bash
pnpm install
npx envpact-cli@0.2.0   # pulls .env from the shared envpact bundle
pnpm dev
```

The dev server runs on `http://localhost:4321`. Hot-reload covers Astro pages,
React islands, MDX, and Tailwind v4 styles.

## Build & deploy

```bash
pnpm build      # static output in ./dist
pnpm preview    # local preview of the built site
pnpm deploy     # wrangler deploy to Cloudflare Workers (oriz-pdf-tools)
```

`pdf.oriz.in` is bound to the `oriz-pdf-tools` Worker via the Cloudflare
dashboard. Cloudflare Pages auto-deploys on push to `main`.

## Stack

- **Astro 6** + **React 19** + **Tailwind v4**
- `@chirag127/oriz-ui` design tokens + shared components
  (`AccountPanel`, `FinishSignIn`, `ContactForm`, `Sidebar`, `AdSlot`)
- Firebase Auth via the shared `oriz-app` project
- `pdf-lib`, `pdfjs-dist`, `tesseract.js`, `mammoth`, `xlsx`, `jspdf`,
  `@dnd-kit/*` for the actual PDF work
- Hosted on Cloudflare Workers (static assets)

## License

MIT.
