# Population Health Calls for Papers Tracker

A running index of open and rolling calls for papers from public health and population health journals — built as a lightweight, searchable reference page.

**[View the live page](https://knechtedapps.github.io/cfps/)**

## What this is

A single-page HTML dashboard listing current calls for papers (special issues, collections, themed sections) from public health–adjacent journals, with search and filtering by journal, topic, and status. It also includes a list of journal sources worth monitoring directly, for anyone who wants to track calls between updates.

## ⚠️ This page is updated manually

There is no automation behind this tracker — no scraper, no scheduled job, no RSS ingestion. Every entry was added by hand after checking the journal's site directly, and the list only reflects what was true as of the date shown in the "Last updated" banner at the top of the page.

**Before submitting to or citing any call listed here, verify the deadline and status directly on the journal's own website.** Calls close early, get extended, or get taken down without notice.

## How to update it

1. Open `population-health-cfp-tracker.html`.
2. Find the `cfps` array near the top of the `<script>` block — each entry is a plain JavaScript object:
   ```js
   {
     journal: "Journal Name",
     title: "Call title",
     desc: "One or two sentence description.",
     deadline: "Due Month Day, Year" | "Rolling submissions",
     status: "open" | "rolling" | "closing",
     tags: ["topic-one", "topic-two"],
     link: "https://..."
   }
   ```
   Add, edit, or remove entries as needed.
3. Update the `LAST_UPDATED` constant just above the `cfps` array (search for `LAST_UPDATED =`). This single line drives both the banner at the top of the page and the compiled-date line in the masthead.
4. Optionally update the `monitorSources` array further down if you want to change the list of journal pages to check.
5. Commit and push. If hosted via GitHub Pages, the change goes live once the build finishes.

No build step, dependencies, or server required — it's a static HTML file with inline CSS and JavaScript.

## Suggesting an addition

If you come across a call for papers that should be added, open an issue or a pull request with:
- Journal name
- Call title and one-line description
- Deadline (or "rolling")
- Link to the official call

## License

Feel free to fork, adapt, or reuse this for your own field or department.
