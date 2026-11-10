# Trove API v3 — Postman Collection

A Postman (v2.1) collection for the **[Trove API v3](https://trove.nla.gov.au/about/create-something/using-api/v3/api-technical-guide)** from the National Library of Australia (22 requests). Trove holds:
- **Australian newspapers** from 1803 to the 1950s and later, with OCR full text
- government gazettes, magazines and newsletters
- books, images, maps, diaries and music
- people and organisation records, and user-curated lists

**Import link** (Postman → Import → Link):
```
https://raw.githubusercontent.com/mikeyeves/Trove-API-Postman/main/Trove_API.postman_collection.json
```

## Setup
1. Create a free Trove account and request an **API key** under Profile → API keys.
2. Paste the key into the collection variable **`trove_key`**. It's sent as `?key=` on every request.
3. The quota is **200 calls per minute**.

## Folders
| Folder | Requests |
|---|---|
| ★ Search | 9 |
| Get records | 5 |
| Titles & contributors | 8 |

Search requests show results in a **Visualizer** table with heading, date, newspaper, page and snippet. The `nextStart` cursor for the next page is shown above the table.

## Genealogy tips
- **Family notices:** `l-category=Family Notices` limits results to birth, death and marriage notices.
- **Date ranges:** use `q=... date:[1900 TO 1930]`, or the `l-decade` filter (e.g. `190` = 1900–1909) together with `l-year`.
- **Full text:** `include=articletext` on **Newspaper article** returns the article's OCR text.
- **Facets:** `facet=decade,state,title,category` shows where and when a name appears.

## Status
Built from the official v3 technical guide. Requests were **not run live**, because every call needs your personal key.

## Related collections
[Library of Congress](https://github.com/mikeyeves/Library-of-Congress-API-Postman) · [WikiTree](https://github.com/mikeyeves/WikiTree-API-Postman) · [Open Archives](https://github.com/mikeyeves/Open-Archives-API-Postman) · [UK & Ireland Archives](https://github.com/mikeyeves/UK-Ireland-Archives-APIs-Postman) · [European Archives](https://github.com/mikeyeves/European-Archives-APIs-Postman)

*Unofficial. Not affiliated with the National Library of Australia. Built from the public API documentation.*
