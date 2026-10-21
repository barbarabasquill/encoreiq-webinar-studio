# EncoreIQ — Webinar-to-Pipeline Studio (Update 2)

An independent, browser-based workspace for B2B Marketing and Sales. No installation, terminal, paid API, automatic email sending, or Salesforce connection required.

## What's new in this update
- Choose **multiple target buyer personas** in Campaign Setup. Create and save different email drafts for each segment and persona.
- Upload one small Salesforce Campaign Member CSV, with six recommended columns: **First Name, Email Address, Company Name, Job Title, Campaign Member Status, Engagement Action**. Optional: **Lead Status, Industry**.
- Engagement Action (e.g. Requested Demo) is separate from attendance status so those contacts aren't counted twice.
- Audience & Segments includes registration, attendance, no-show, demo-interest rates; webinar-type-aware **Repeat / Improve / Stop or Reconsider / Try Next** guidance; optional campaign attendance goal; manual-results mode; and downloadable performance report.
- Download audience assignments, segment/persona email drafts, and webinar-content roadmap.
- Edit webinar descriptions, URLs, CTA links, and copy. Copy a Claude prompt for optional Firecrawl-assisted research outside the app.

## Upload to your existing GitHub repo
1. Open your existing EncoreIQ repository on GitHub.
2. Replace the **root `index.html`** file, **`css/styles.css`**, **`js/app.js`**, and **root `README.md`** with these updated versions. (Do not upload the ZIP file as a website file.)
3. Easiest approach: GitHub **Add file → Upload files** and drag the *contents* of this extracted package, retaining folder paths. Confirm GitHub detects replacements, then **Commit changes**.
4. Keep GitHub Pages at Settings → Pages → Deploy from a branch → main → /(root). Refresh your live site after the deployment completes.

## Example Salesforce CSV
A downloadable **`salesforce-webinar-sample.csv`** with entirely fictional contacts is included. You can also click **Download sample CSV** in the app.

Recognized Salesforce header alternatives include `Email`, `Status`, `Company`, and `Title`. CSV is processed locally in the browser, not on a server. Email is required to identify duplicate rows. If the same email appears in multiple campaign rows, we keep a single record and prefer a recognized attendance status, but manually review any conflicts.

## Tests
1. Select 3 personas in Campaign Setup → all 3 appear beneath the selector; changing the persona in Email Studio changes the recommended draft.
2. Load fictional samples → performance dashboard displays registrants, live attendees, no-shows and demo requests (one person may both attend and request a demo).
3. Upload the included Salesforce sample CSV → preview and dashboard populate, and CSV export downloads.
4. Switch to **Use manually entered totals** and enter 500 registered, 325 attended, 175 no-shows, 48 demo requests → **65.0% attendance** and **9.6% demo request rate**.
5. Enter an invalid count such as -2 or 1.5 → error explains that counts must be nonnegative whole numbers; attended + no-shows greater than registered also shows an error.
6. Enter an attendance goal of 70% using the manual example → Improve section flags a shortfall against *your* goal.
7. Blank required manual fields → readable validation error.
8. Invalid audience CSV with no Email or Status column → readable validation error.
9. Fill email CTA with `not-a-url` and click Save → readable URL error.
10. Download performance CSV and audience assignments; confirm actual calculations and editable recommendations are present.

## Honest scope and safety
The application does **not** automatically read webinar URLs, scrape websites, connect to Firecrawl or Clay, use a generative AI API, write Salesforce records, or send messages. It creates **rules-based, editable draft recommendations** based on provided webinar notes and audience statuses. The generated Claude research prompt is optional and is not sent anywhere by EncoreIQ. Check permissions, privacy and costs separately before using external services. Never upload real CRM contacts to the public GitHub repository; load authorized CSV data through the live browser app only. Audience contacts stay in the current browser session. General campaign settings can be stored in browser local storage. Follow organization consent/suppression rules before using exports for outreach. Imported records may have pending or inconsistent statuses; the dashboard identifies uncertainty rather than implying unverified rates are benchmarks.


## V3 changes
- Dedicated Webinar performance navigation item, with existing manual/CSV analysis.
- Campaign-member denominator clearly labeled as a proxy for registrations; separates replay and partial viewers, while flagging unknown statuses.
- Email Studio has a three-touch selector. Generate, edit, and save each touch separately. Export selected three-touch sequence and a full campaign plan including touch numbers.
- No automatic outreach or CRM writes. Claimed webinar details come only from marketer-supplied notes; webinar URLs are not scraped.


## V3 Enhanced update
- Branding: “Created by Barbara Basquill” near the logo and a © 2026 Barbara Basquill footer. The SAMPLE WORKSPACE badge was removed entirely.
- Follow-up Studio: three subject line alternatives; improved, editable, persona-aware emails based only on the webinar text entered; matched CTAs from user-verified resource links; recipient preview and copy/export with actual CTA text. No automatic website research.
- Review & Export: View each of the three CSV outputs before downloading (first 30 rows shown; export includes all rows). Audience preview may contain personally identifiable information; use authorized exports only and shared devices cautiously.
- Local-only: Salesforce contacts are not sent to any server. Saved settings are in localStorage; imported records and drafts are in this browser session.
- Safety: Missing CTA URLs are highlighted; a URL alone does not provide webinar content; pasted notes still require human fact-checking.

### GitHub upload
Replace the five items at the repository root: index.html, css/styles.css, js/app.js, README.md, salesforce-webinar-sample.csv. Commit directly to main and refresh the published site (Cmd+Shift+R on Mac).
