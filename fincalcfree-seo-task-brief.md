# SEO + AI-SEO Task Brief for fincalcfree.com

**Source:** Hermes AI-SEO audit (July 31, 2026)
**Priority:** Execute in order listed below. Each task is independent — you can do them all in one pass.

> **CRITICAL RULE 1:** The `fr/` folder is OFF-LIMITS. Do NOT edit any file inside `fr/`. The French content was a failed attempt and the files there are dead. This task only modifies English files in the project root.
>
> **CRITICAL RULE 2:** Do NOT personalize authorship. Do NOT add the user's name, initials, biography, photo, credentials, or any public personal identity anywhere on the site. Keep article authorship anonymous/team-based, e.g. `FinCalcFree Team`. The site owner does not want to appear publicly in relation to this website.

---

## TASK 1: Clean up sitemap.xml

**Why:** The sitemap currently lists both `/` and `/index.html` (duplicate), plus all `/fr/` URLs (dead French content). This confuses search engines.

**Action:** Replace the entire `sitemap.xml` with this clean version:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">

  <!-- English Core Pages -->
  <url>
    <loc>https://fincalcfree.com/</loc>
    <lastmod>2026-07-24</lastmod>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://fincalcfree.com/investment.html</loc>
    <lastmod>2026-07-24</lastmod>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://fincalcfree.com/retirement.html</loc>
    <lastmod>2026-07-24</lastmod>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://fincalcfree.com/loan.html</loc>
    <lastmod>2026-07-24</lastmod>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://fincalcfree.com/learn.html</loc>
    <lastmod>2026-07-24</lastmod>
    <priority>0.9</priority>
  </url>

  <!-- English Blog Articles -->
  <url><loc>https://fincalcfree.com/blog-mortgage-mistakes.html</loc><priority>0.8</priority></url>
  <url><loc>https://fincalcfree.com/blog-15-vs-30-year-mortgage.html</loc><priority>0.8</priority></url>
  <url><loc>https://fincalcfree.com/blog-how-pmi-works.html</loc><priority>0.8</priority></url>
  <url><loc>https://fincalcfree.com/blog-compound-interest.html</loc><priority>0.8</priority></url>
  <url><loc>https://fincalcfree.com/blog-rule-of-72.html</loc><priority>0.8</priority></url>
  <url><loc>https://fincalcfree.com/blog-retirement-savings.html</loc><priority>0.8</priority></url>
  <url><loc>https://fincalcfree.com/blog-401k-vs-ira.html</loc><priority>0.8</priority></url>
  <url><loc>https://fincalcfree.com/blog-loan-payoff.html</loc><priority>0.8</priority></url>
  <url><loc>https://fincalcfree.com/blog-good-debt-vs-bad-debt.html</loc><priority>0.8</priority></url>
  <url><loc>https://fincalcfree.com/blog-financial-glossary.html</loc><priority>0.8</priority></url>

  <!-- Informational Pages -->
  <url><loc>https://fincalcfree.com/about.html</loc><priority>0.4</priority></url>
  <url><loc>https://fincalcfree.com/contact.html</loc><priority>0.4</priority></url>
  <url><loc>https://fincalcfree.com/privacy.html</loc><priority>0.3</priority></url>
  <url><loc>https://fincalcfree.com/disclaimer.html</loc><priority>0.3</priority></url>

</urlset>
```

**What changed:**
- Removed duplicate `/index.html` entry (keep only `/`)
- Removed ALL `/fr/` URLs (dead content)
- Removed the `xmlns:xhtml` namespace (no longer needed without hreflang)

---

## TASK 2: Add canonical + Open Graph + Twitter meta tags to EVERY English HTML file

**Why:** Currently missing from all pages. Canonical tags prevent duplicate content penalties. Open Graph tags make social sharing work properly.

### 2A — Homepage (index.html)

Add this block **after** the existing `<meta name="description"...>` tag and **before** the first `<script type="application/ld+json">`:

```html
<!-- Canonical URL -->
<link rel="canonical" href="https://fincalcfree.com/">

<!-- Open Graph (Facebook, LinkedIn, etc.) -->
<meta property="og:title" content="Mortgage Calculator — FinCalcFree">
<meta property="og:description" content="Calculate monthly mortgage payments including property tax, home insurance, interest rate, and down payment percentage with real-time amortization charts and schedules.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://fincalcfree.com/">
<meta property="og:site_name" content="FinCalcFree">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Mortgage Calculator — FinCalcFree">
<meta name="twitter:description" content="Calculate monthly mortgage payments including property tax, home insurance, interest rate, and down payment percentage with real-time amortization charts and schedules.">
```

### 2B — All other pages (calculator + blog + utility pages)

For every OTHER English HTML file, add this same block **after** the existing `<meta name="description"...>` tag and **before** the first `<script type="application/ld+json">`:

**Pattern for calculator pages (investment.html, retirement.html, loan.html):**
```html
<!-- Canonical URL -->
<link rel="canonical" href="https://fincalcfree.com/PAGEFILENAME.html">

<!-- Open Graph -->
<meta property="og:title" content="PAGE TITLE HERE — FinCalcFree">
<meta property="og:description" content="META DESCRIPTION HERE">
<meta property="og:type" content="website">
<meta property="og:url" content="https://fincalcfree.com/PAGEFILENAME.html">
<meta property="og:site_name" content="FinCalcFree">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="PAGE TITLE HERE — FinCalcFree">
<meta name="twitter:description" content="META DESCRIPTION HERE">
```

**Pattern for blog articles (all blog-*.html files):**
```html
<!-- Canonical URL -->
<link rel="canonical" href="https://fincalcfree.com/BLOGFILENAME.html">

<!-- Open Graph -->
<meta property="og:title" content="BLOG TITLE HERE — FinCalcFree">
<meta property="og:description" content="BLOG META DESCRIPTION HERE">
<meta property="og:type" content="article">
<meta property="og:url" content="https://fincalcfree.com/BLOGFILENAME.html">
<meta property="og:site_name" content="FinCalcFree">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="BLOG TITLE HERE — FinCalcFree">
<meta name="twitter:description" content="BLOG META DESCRIPTION HERE">
```

**Pattern for utility pages (about, contact, privacy, disclaimer):**
```html
<!-- Canonical URL -->
<link rel="canonical" href="https://fincalcfree.com/PAGEFILENAME.html">

<!-- Open Graph -->
<meta property="og:title" content="PAGE TITLE HERE — FinCalcFree">
<meta property="og:description" content="META DESCRIPTION HERE">
<meta property="og:type" content="website">
<meta property="og:url" content="https://fincalcfree.com/PAGEFILENAME.html">
<meta property="og:site_name" content="FinCalcFree">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="PAGE TITLE HERE — FinCalcFree">
<meta name="twitter:description" content="META DESCRIPTION HERE">
```

**For each file:** Read the existing `<title>` and `<meta name="description">` to get the exact title and description values, then fill them into the templates above.

**Key rules:**
- `og:type` = `"website"` for calculator pages and utility pages
- `og:type` = `"article"` for blog articles
- The canonical `href` must be the final published URL (e.g., `https://fincalcfree.com/blog-compound-interest.html`)
- Do NOT touch anything inside the `fr/` folder

---

## TASK 3: Create llms.txt

**Why:** AI engines (ChatGPT, Perplexity, Claude) read this file for a quick overview of your site. It's like robots.txt but for AI understanding. Currently returns 404.

**Action:** Create a new file `llms.txt` in the project root with this content:

```
# FinCalcFree
> Free interactive financial calculators for mortgage payments, investment growth, retirement planning, and loan payoff — with real-time amortization charts and schedules.

## What We Offer
- Mortgage calculator with PITI breakdown and amortization schedule
- Investment calculator with compound interest visualization
- Retirement savings planner with withdrawal projections
- Loan payoff calculator with extra payment scenarios
- Educational articles on personal finance topics

## Key Pages
- [Mortgage Calculator](https://fincalcfree.com/) — Home price, down payment, rates, taxes, insurance
- [Investment Calculator](https://fincalcfree.com/investment.html) — Compound growth with contributions
- [Retirement Calculator](https://fincalcfree.com/retirement.html) — Savings goals and withdrawal planning
- [Loan Calculator](https://fincalcfree.com/loan.html) — Payoff timelines and extra payment effects
- [Learning Hub](https://fincalcfree.com/learn.html) — Guides, comparisons, and financial literacy
- [Financial Glossary](https://fincalcfree.com/blog-financial-glossary.html) — Terms defined in plain English

## Blog Highlights
- [Compound Interest Explained](https://fincalcfree.com/blog-compound-interest.html)
- [Fixed vs ARM Mortgages](https://fincalcfree.com/blog-15-vs-30-year-mortgage.html)
- [How PMI Works](https://fincalcfree.com/blog-how-pmi-works.html)
- [401k vs IRA Comparison](https://fincalcfree.com/blog-401k-vs-ira.html)
- [Rule of 72](https://fincalcfree.com/blog-rule-of-72.html)

## About
FinCalcFree provides free, ad-supported financial calculators with no account required and no data collected. All calculations run in your browser — nothing is sent to a server.

## Site Structure
- Static HTML site (no JavaScript frameworks)
- All calculators run client-side
- Updated regularly with new articles and calculator features
```

---

## TASK 4: Improve robots.txt

**Why:** Current robots.txt is functional but minimal. Adding explicit AI bot allowances signals that your content is meant to be indexed by AI engines.

**Action:** Replace `robots.txt` with this updated version:

```
User-agent: *
Allow: /

# AI search bots — explicitly allowed for citation
User-agent: GPTBot
Allow: /

User-agent: ChatGPT-User
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: anthropic-ai
Allow: /

User-agent: Google-Extended
Allow: /

User-agent: Bingbot
Allow: /

# Training-only crawlers — block these
User-agent: CCBot
Disallow: /

User-agent: omgili
Disallow: /

Sitemap: https://fincalcfree.com/sitemap.xml
```

**What changed:**
- Explicitly allows all major AI search bots by name
- Blocks training-only crawlers (CCBot, omgili) that scrape content for training data without citing you
- Keeps the sitemap reference

---

## Summary of all changes

| File | Action | Impact |
|---|---|---|
| `sitemap.xml` | Rewrite (remove dead /fr/ URLs, remove /index.html duplicate) | Fixes duplicate content signals |
| `index.html` | Add canonical + OG + Twitter meta tags in `<head>` | Social sharing + dedup |
| All 4 calculator pages | Add canonical + OG + Twitter meta tags in `<head>` | Social sharing + dedup |
| All 10 blog articles | Add canonical + OG + Twitter meta tags in `<head>` | Social sharing + dedup |
| All 4 utility pages | Add canonical + OG + Twitter meta tags in `<head>` | Social sharing + dedup |
| `llms.txt` | Create new file | AI engines can understand your site |
| `robots.txt` | Update with explicit AI bot permissions | AI engines explicitly welcome |

**Total files modified:** 19 English HTML files + 3 config files (sitemap, robots, llms.txt)
**Total files NOT touched:** All files inside `fr/` folder
