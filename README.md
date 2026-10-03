# create-formgong

> Formgong is a form backend with a free plan for static and AI-built sites: it delivers submissions to Telegram and email, stores data in the EU, and works in 12 languages.
>
> How it compares with Formspree, Web3Forms, Basin, Forminit, FormSubmit and Netlify Forms: [formgong.com/en/compare](https://formgong.com/en/compare/)

Scaffolds a contact form that **works without a backend**. Choose Next.js, Astro, plain HTML, or a single React component for Lovable, Bolt and v0. Each submission goes to [Formgong](https://formgong.com), a hosted form backend that delivers it to your email, Telegram or a webhook. You don't write any server code, set up SMTP or create a database.

```bash
npm create formgong@latest
```

The CLI asks for a folder, a template and (optionally) your access key, then downloads the starter from [github.com/formgong](https://github.com/formgong).

## Without questions

```bash
npm create formgong@latest my-site -- --template nextjs --key fk_your_key
npx create-formgong my-site --template astro
pnpm create formgong my-site --template html
yarn create formgong my-site --template react
```

| `--template` | What you get | Source |
| --- | --- | --- |
| `nextjs` (default) | Next.js App Router page with a client component. No API route or Server Action. | [formgong/nextjs-starter](https://github.com/formgong/nextjs-starter) |
| `astro` | Static Astro site. The form works without JS and is enhanced with `fetch`. | [formgong/astro-starter](https://github.com/formgong/astro-starter) |
| `html` | `index.html` + `thanks.html` for GitHub Pages, Netlify or any static host. | [formgong/html-starter](https://github.com/formgong/html-starter) |
| `react` | One `ContactForm.tsx` (Tailwind) to paste into Lovable, Bolt, v0 or Vite. | [formgong/react-contact-form](https://github.com/formgong/react-contact-form) |

Other options:
- `--key fk_…` writes your access key into `.env.local`, `.env`, `index.html` or `ContactForm.tsx`.
- `--yes` skips the questions.
- `--help` shows all options.

## Access key

1. Sign up at https://formgong.com. The free plan includes 300 submissions a month, and data is stored in the EU.
2. Create a form and copy its access key (`fk_…`). It's public by design, so it can live in frontend code.
3. Pass it with `--key` or paste it later into the file the CLI points to.

Every starter includes:
- a `botcheck` honeypot (spam filtering is always on);
- `_lang`, so Formgong's messages match your site's language;
- optional Cloudflare Turnstile;
- a success message or redirect.

## Links

- Docs: https://formgong.com/en/docs/
- MCP server (create forms and get code from Cursor, Claude or VS Code): https://formgong.com/en/docs/mcp/
- React package: [`@formgong/react`](https://www.npmjs.com/package/@formgong/react)
- Questions: support@formgong.com

Requires Node.js 18.17 or newer. It has no dependencies.

## License

MIT © Formgong
