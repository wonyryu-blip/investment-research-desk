# Research Desk registration

When the user requests research saved to this desk, use the connected GitHub repository wonyryu-blip/investment-research-desk, branch main. Read this file and current data/reports.json before each update. No Sites editor or Notion is needed. Do not put credentials or private personal information in this public repository.

1. Verify primary sources and dates; distinguish facts, management guidance, analyst interpretation, and market price timestamp/timezone. Do not invent figures or future market moves. Include source URLs and qualification for unverified transcripts.
2. Preserve all existing reports. Stable report id format: ticker-topic-YYYYMMDD. Update matching ids for followups instead of creating duplicates. Save UTF-8 Markdown to reports/<id>.md and identical body in data/reports.json.
3. Each report requires id, title, date (YYYY-MM-DD), tickers array, matching companies array, category, status, summary, body. Set top-level updated to the latest registration date. Cross-company reports may have multiple tickers. One report remains one report in counts.
4. Commit content and index atomically. Preserve unrelated repository files. Check current main head; use expected_sha when updating the ref. On conflict reread and merge; never force push.
5. Verify JSON parses, ids are unique, ticker/company lengths match, Markdown bodies match files, and source links use HTTP(S). Verify GitHub Pages publication; report separately if saved but deployment is pending. Return the report link https://wonyryu-blip.github.io/investment-research-desk/#report/<id> and commit link.

Public browsing needs no login. Writes require the user's GitHub connector authorization. New ChatGPT conversations must be given this repo or desk URL so the workflow can be located. Never claim an automatic background or permanent account-wide integration exists without verifying it.

## Migrated archive

Keep companies metadata in data/reports.json and archive snapshots intact. Preserve all fields, historical dates, classification (ipo/kr/global), report type/category and pending flags. Do not count pending records as available reports. Financial values in company profiles use millions of the stated currency; unknown values must remain unknown. External official materials remain links, not locally stored full reports. Do not restore the personal Drive URL or internal registration notes excluded by publication review. Add newly researched company profiles when registering future reports, preserving existing company IDs.
