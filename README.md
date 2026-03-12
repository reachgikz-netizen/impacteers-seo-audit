# 🔍 Father's Content Audit Tool

> Built by Girish — Father of SEO · Powered by Pyodide · 100% Free · Zero Server · Zero Cost · Forever

A professional-grade SEO content audit tool that runs **entirely in your browser**. Upload a `.docx` file or paste a live URL — get a deep 16-signal audit with exact sentence-level issues, E-E-A-T scoring, AI citation analysis, and a colour-coded Excel report. No backend. No login. No subscription.

---

## 🚀 Live Tool

👉 **[https://reachgikz-netizen.github.io/father-s-seo-content-audit](https://reachgikz-netizen.github.io/father-s-seo-content-audit)**

---

## ✨ Key Features

### Two Audit Modes

| Mode | How It Works |
|------|-------------|
| **Upload .docx** | Upload one or more Word documents — supports multiple files |
| **Audit Live URL** | Paste any public URL — the tool fetches, parses and audits the live page directly |

### Multi-Article Detection

When a single `.docx` contains multiple articles (common for interns submitting 2+ articles in one doc), the tool automatically:
- Detects multiple H1 headings
- Filters out label-only headings like `"Pillar Topic 1 :"`
- Extracts each real article title
- Asks for a separate target keyword per article
- Audits and tabs each article individually

---

## 🧠 16 SEO Signals Audited

| Signal | What's Checked |
|--------|---------------|
| 🔑 **Keyword Density** | Frequency, percentage, stuffing detection (ideal: 0.5–2.5%) |
| 🏷️ **Heading Structure** | H1 uniqueness, H2/H3 count, label-H1 filtering |
| 📖 **Readability** | Flesch Reading Ease score, average sentence length |
| 🖼️ **Images & Alt Text** | Total images, missing alt tag count |
| 🔗 **Internal Links** | Count of internal vs external links |
| ⚓ **Anchor Text Quality** | Descriptive anchors vs generic ("click here") |
| 🏷️ **Meta Tags** | Title length (ideal 50–60 chars), meta description (ideal 140–160 chars) |
| ❓ **FAQ Detection** | FAQ section presence for featured snippet eligibility |
| 🤖 **AI Citation Score** | 5-dimension E-E-A-T scoring engine (see below) |
| 🧩 **LSI Terms** | 60+ career-niche LSI terms mapped and scored |
| 🏢 **Entity Detection** | Named entities: companies, institutions, tools, platforms |
| 🌐 **Semantic Coverage** | Pillar-aligned semantic terms + missing term suggestions |
| 💬 **Sentiment Score** | Positive / Neutral / Negative with word-level breakdown |
| 🎙️ **Tone of Voice** | Formal / Casual / Balanced detection |
| 🚀 **Brand Alignment** | Platform-specific terms and brand relevance score |
| 📣 **CTA Detection** | Conversion call-to-action presence and quality |

---

## 🤖 AI Citation Score — 5-Dimension Engine

Rebuilt from 2026 SEO research: Ahrefs E-E-A-T framework, Sitebulb grounding budget study, SALT.agency Query Fan-Out analysis, HubSpot Entity SEO guide, and SEJ's Demand SEO model.

| Dimension | Max | What It Checks |
|-----------|-----|----------------|
| **Authority Signals** | 25 | Named sources (NASSCOM, LinkedIn, Forbes, IIT, McKinsey…) + citation phrases |
| **E-E-A-T Signals** | 25 | Experience markers, expertise language, trust dates ("as of 2026"), penalises filler openers |
| **Statistical Evidence** | 20 | Percentages, ₹/$ numbers, year-dated stats, comparisons ("3x faster", "40% higher") |
| **Passage Extractability** | 15 | % of paragraphs opening with direct answers, density of short standalone sentences |
| **Entity Specificity** | 15 | Named entities paired with action verbs ("LinkedIn reported", "study found") |

---

## ✍️ Exact Issue Extraction — For Writers

Every audit includes sentence-level issues so writers know exactly what to fix:

| Type | What It Finds |
|------|--------------|
| 🔴 **Long Sentences** | Over 35 words — shown verbatim with fix tip |
| 🟡 **Passive Voice** | Passive constructions flagged and highlighted |
| 🔴 **Keyword Stuffing** | Sentences where keyword appears 3+ times |
| 🟡 **Weak Openers** | Sentences starting with "There is / It is / This is" |
| 🔵 **Missing Transitions** | Isolated paragraphs with no transition words |
| 🟡 **Thin Paragraphs** | Single-line paragraphs that need expanding |

---

## 📊 Excel Report

Every audit generates a colour-coded `.xlsx`:

- **Summary Dashboard** — all articles/URLs in one sheet with scores and top issues
- **Per-article sheets** — full 16-signal breakdown with green/yellow/red cells
- **AI Citation Breakdown** — all 5 sub-scores detailed
- **Exact Issues** — writer-ready sentence extracts with fix recommendations

---

## 🔧 How to Use

### Option A — Upload .docx
1. Open the live tool
2. Select the **Upload .docx File** tab
3. Drop or browse your `.docx` file(s)
4. If multiple articles detected, enter a keyword per article
5. Click **⚡ Run SEO Audit**
6. Review on screen → download Excel report

### Option B — Audit Live URL
1. Open the live tool
2. Select the **🌐 Audit Live URL** tab
3. Paste a public URL (e.g. `https://blog.impacteers.com/your-article`)
4. Add more URLs if needed
5. Enter target keyword → **⚡ Audit URL**
6. Results show with a 🌐 URL badge and clickable source link

> **CORS Note:** Some websites block browser-based fetching. If a URL fails, download the page as a `.docx` and use Upload mode instead.

---

## 📦 Deployment

### Repo structure
```
father-s-seo-content-audit/
├── index.html              ← The entire tool (Python + UI in one file)
├── README.md
├── .gitignore
└── .github/
    └── workflows/
        └── deploy.yml      ← Auto-deploy to GitHub Pages on push
```

### Steps
```bash
git add .
git commit -m "Deploy Father's Content Audit Tool"
git push origin main
```

Then: **Settings → Pages → Source → GitHub Actions** → Save.  
Live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME` in ~60 seconds.

### Updating the tool
Only `index.html` ever needs to be replaced. The entire tool — Python engine, UI, audit logic, CSS — lives in that one file. Replace → commit → deployed.

---

## 🛡️ Privacy

Everything runs 100% inside your browser:
- `.docx` files are never uploaded to any server
- URLs are fetched directly by your browser (no proxy)
- No analytics, no tracking, no data collection
- Works offline after first load (Pyodide cached by browser)

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Python Runtime | [Pyodide](https://pyodide.org) — CPython compiled to WebAssembly |
| Document Parsing | `python-docx` |
| HTML Parsing | Built-in regex parser (no external lib needed) |
| Excel Generation | `openpyxl` |
| Hosting | GitHub Pages (free) |
| Font | Poppins (Google Fonts) |
| Build step | None — pure HTML/CSS/JS |

---

## 🗺️ Roadmap

- [ ] Rank Tracker — 2000+ keywords, enterprise scale
- [ ] Keyword Research + Clustering — SEMrush CSV + SERP grouping
- [ ] Master Dashboard — combined report across all modules
- [ ] Competitor URL Comparison — your article vs competitor side by side
- [ ] Bulk URL Mode — paste a sitemap for batch auditing

---

Built with ❤️ for Girish — Father of SEO at Impacteers
