# ShareVolume_019a0bf1-1ccf-72b8-ac80-b5e2c305225e

Your assigned company: 3M (MMM), CIK 0000066740.

Fetch https://data.sec.gov/api/xbrl/companyconcept/CIK0000066740/dei/EntityCommonStockSharesOutstanding.json (set a descriptive User-Agent per SEC guidance).
Read `.entityName`. Filter `.units.shares[]` for entries whose `fy` > "2020" and
includes a numeric `val`.
Save `data.json` with this structure:
`{"entityName": "3M", "max": {"val": ..., "fy": ...}, "min": {"val": ..., "fy": ...}}`
where `max` and `min` refer to the highest and lowest `.val`. Break ties however you like.

Render a visually appealing `index.html` where:
- `<title>` and `<h1>` must include the live `entityName`.
- The max/min figures are clearly marked with these IDs:
  `share-entity-name`,
  `share-max-value`, `share-max-fy`,
  `share-min-value`, `share-min-fy`.

If the page is opened as `index.html?CIK=0001018724` (or any other 10-digit CIK),
`fetch()` from the SEC endpoint for that CIK using any proxy, e.g. AIPipe,
replace every ID listed above and the title and H1 without reloading the page.

Also commit the attachment uid.txt as-is.

## Overview
This repository contains a static web application built for the specified task.

## Setup
No build step required. The app is served via GitHub Pages.

## Usage
Open [https://iitm-iyy.github.io/ShareVolume_019a0bf1-1ccf-72b8-ac80-b5e2c305225e/](https://iitm-iyy.github.io/ShareVolume_019a0bf1-1ccf-72b8-ac80-b5e2c305225e/) in your browser.

## Code Explanation
- `index.html`: The main application file, generated to meet task requirements.
  - Loads required libraries via CDN.
  - Implements the task as per the provided brief.

## License
MIT
