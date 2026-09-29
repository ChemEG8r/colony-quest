# Colony Quest

Colonial America study practice for VJ, built from Mr. Jack's study guide:
key terms (democracy, social contract, liberty, boycott, repeal, compact),
the three colonial regions, the road to revolution (First Continental
Congress, Proclamation of 1763, Fundamental Orders of Connecticut, John
Locke, mercantilism), and the five founding documents (Magna Carta,
Mayflower Compact, English Bill of Rights, Cato's Letters, Common Sense).

Note: the regions content here is the historically correct version — the
filled-in worksheet had modern-day state facts and misplaced several
colonies, so the app teaches the right ones.

- Each quiz is 15 questions drawn at random from a 50-question bank, mixing
  multiple choice and fill-in-the-blank (typing forgives small misspellings).
- Instant grading with a one-line "why" for every question.
- A phone-sized study sheet covering the whole guide, tables included.
- History records every quiz with the exact misses; synced across devices
  when hosted on Cloudflare Pages, per-device anywhere else.

## Hosting

Single static `index.html`, no build step. Cloudflare Pages with a Pages
Function (`functions/api/scores.js`, Workers KV bound as `SCORES`) keeping
one shared history at `/api/scores`. Deployed manually with
`npx wrangler pages deploy . --project-name colony-quest --branch main`
(needs `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID`).
