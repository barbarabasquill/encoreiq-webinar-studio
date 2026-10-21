# EncoreIQ — Webinar-to-Pipeline Studio

A standalone, browser-first webinar follow-up planner for Marketing and Sales. No terminal, build pipeline, paid API, CRM write, or outbound email connection is needed.

## What it does
- Enter webinar and company website URLs and paste a webinar description or transcript.
- Copy a research prompt for Claude to use with optional, separately configured Firecrawl; paste the findings back.
- Import Salesforce/webinar CSVs with basic validation, status normalization and duplicate detection.
- Review/edit segment-specific follow-up email drafts and two CTA recommendations.
- Plan additional webinar topics, content gaps, next actions, and illustrative pipeline.
- Export campaign plan, audience assignments and content roadmap as CSV files.

## Deploy on GitHub Pages
Upload `index.html`, the `css` folder and the `js` folder to the **root** of this repository. In **Settings → Pages → Build and deployment**, choose **Deploy from a branch**, **main**, **/(root)**, and Save. The site will be available at `https://YOUR-USERNAME.github.io/encoreiq-webinar-studio/` after publishing.

## Privacy and limitations
All demo contacts are fictional. Imported audience data remains in the current browser session, not on a server. Non-contact campaign settings may be stored in browser localStorage. Avoid shared devices for real data. CSV exports download to your computer and must be handled in accordance with your organization's privacy policies.

**This version does not fetch or read URLs.** Firecrawl, Claude and Clay are **not integrated**. The optional Claude prompt is copied to your clipboard and can be used in a separately configured Claude environment; any external service's fees, permissions, and data policies are its own. Content and email recommendations are local, editable rules-based starting points, not verified research or AI-generated messages. CTA URLs must be verified by the marketer. No emails are sent, and no Salesforce data is changed.

## Quick test cases
1. **Blank pipeline rate:** clear Qualified Lead Rate and click Calculate → a readable error appears.
2. **Invalid rate:** enter 120 for Meeting Rate → an error says rates must be 0–100%.
3. **Invalid CSV:** import CSV without Email or Status columns → error identifies missing columns.
4. **Invalid CTA:** enter `not-a-url` for CTA 1 and Save → validation error appears.
5. **Successful example:** click Load fictional sample records, Generate draft, add a valid `https://example.com/...` URL for each selected CTA, Save draft, and Export campaign plan → a CSV downloads.
6. **Duplicate record:** upload CSV with repeated email rows → only first is retained and duplicates are counted.
7. **Webinar research:** supply text in webinar notes and click Analyze → a source-limited topic summary appears; no remote fetch occurs.

## Folder layout
```
index.html
css/styles.css
js/app.js
README.md
```
