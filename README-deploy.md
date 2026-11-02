# Website deployment prep (site/ → live for $0)

## Cheapest reliable options (USD, Nov 2026 knowledge, verify at purchase — $0 SPEND AUTHORISED, do not buy)
1. **GitHub Pages — RECOMMENDED $0**: free static hosting, HTTPS, custom domain optional later (~$10-15/yr domain only, NOT authorised). Why: `gh` already authed (abhishekshahi), site is 2 static HTML files, deploy = `gh repo create leadrescue-site --public --source=site --push` + enable Pages. Bandwidth 100GB/mo — plenty for demo traffic.
2. Cloudflare Pages $0: free, fast, same static upload; needs Cloudflare account (none connected) — second choice.
3. Netlify Drop $0: drag-and-drop; needs account — third choice.
Avoid: paid shared hosting ($5-15/mo), Vercel (fine but account needed; no advantage over GH Pages here).

## Deploy steps (owner runs or authorises; ~10 min, $0)
1. `cd money-mission && gh repo create leadrescue-site --public --source=site --push`
2. Repo Settings → Pages → Deploy from branch → main / (root) → Save → live URL `https://<user>.github.io/leadrescue-site/`
3. Replace demo/outreach `[link]` placeholders with live URL. Test: both pages load, demo runs, no console errors.
4. Later (needs approval + $): custom domain (Namecheap/Cloudflare ~$10-15/yr) + free TLS via Pages.

## Pre-deploy checklist
- [x] index.html + demo.html parse clean, no external keys, mock-data labels present
- [ ] Replace placeholder booking/contact links with owner-approved URLs
- [ ] Add honest footer (solo operator, no fake testimonials) — present; re-verify post-deploy
- [ ] Confirm no PII/real prospect phones in site files (grep before push)
