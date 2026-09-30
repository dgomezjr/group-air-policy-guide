# Group Air Policy & Procedures — Classic Vacations

An internal reference for Reservations and Customer Service: how to spot a
Group Air booking, move it through the eight-stage lifecycle, and answer
advisor questions mid-call without digging through policy documents.

It's a single HTML file. No build step, no server, no dependencies to
install. It runs on GitHub Pages and can be embedded in SharePoint via
iframe, the same way as the RSS Operations guide and the other reference
tools.

## What's in the guide

| Section | What it covers |
|---|---|
| **Mid-call answers** | Search-first view: the quick answers agents need while an advisor is on the line |
| **Lifecycle (8 stages)** | Identify → Request → Proposal → Accept → Deposit & deadlines → Names & seats → Changes → Service |
| **Carriers** | Per-airline group rules: minimum size, deviations, name-change allowance, deposits, check-in |
| **Policies** | The rules in plain language, each with the reason behind it and a link to its stage |
| **Where groups go wrong** | Common mistakes and how to avoid them |
| **Checklists** | Step-by-step lists for each hand-off point |

### Shortcuts

| Key | Action |
|---|---|
| `/` or `Ctrl+K` | Open search |
| `↑` `↓` `Enter` | Move through and open search results |
| `Esc` | Close search |
| `←` `→` | Move between tabs |

Every section has its own link (for example, `…/#deposit`), so agents can
share a link that goes straight to the right answer.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole guide: layout, styling, content, and search |
| `README.md` | This file |

## Updating content

All content is in plain data lists near the bottom of `index.html`, in the
`DATA` section. You don't need to touch any layout code.

| List | Holds |
|---|---|
| `LINKS` | External links, such as the [Group Air Request Form](https://app.smartsheet.com/b/form/99b409a65fcd4459bc6178490b31c681) |
| `STAGES` | The eight lifecycle stage names |
| `TASKS` | Mid-call task answers |
| `CARRIERS` | Airline-by-airline group rules |
| `LANES`, `CHANNELS` | Who owns what, and how to reach them |
| `POLICIES` | Policy statements: rule, reason, and linked stage |
| `TRAPS` | "Where groups go wrong" items |
| `CHECKS` | Checklists |
| `PATHS` | Guided decision paths |
| `SUGGEST` | Suggested search terms shown in the search box |

Search indexes all of this automatically, so a new entry becomes searchable
as soon as it's saved.

For anything more than a small wording fix, send Claude the updated policy
text (a redline, transcript, or just the new wording) and have it rebuild
the affected entries. That keeps formatting and cross-links consistent.

**Before publishing any change:** open `index.html` in a browser and check
that the page loads and search works. A missing comma or quote in a data
list will blank the page.

## Publishing on GitHub Pages

1. Create a new **public** repository on GitHub named `group-air-policy-guide`.
   Public means anyone with the link can read the guide, so keep
   confidential material (contract rates, internal contacts) out of it.
2. Upload `index.html` and `README.md` to the repository's `main` branch.
3. Go to **Settings → Pages**. Under **Build and deployment**, choose
   **Deploy from a branch**, then select `main` and `/ (root)`. Save.
4. After a minute or two, the guide is live at
   `https://dgomezjr.github.io/group-air-policy-guide/`.

To update the live guide, commit the new `index.html` to `main`. Pages
republishes automatically.

## Embedding in SharePoint

Add an **Embed** web part to the SharePoint page and paste:

```html
<iframe src="https://dgomezjr.github.io/group-air-policy-guide/"
        width="100%" height="900" style="border:0"></iframe>
```

If SharePoint blocks the embed, a site admin needs to add
`dgomezjr.github.io` to the site's allowed embed domains
(**Site settings → HTML Field Security**).

## Keep current

- **Review date.** The footer says *Updated September 2026*. Change it
  whenever the policy content changes.

---

Brand: Classic Vacations Jan 2026 guide (Onyx / Pearl / Swell palette,
Archivo + JetBrains Mono via Google Fonts).
