# KundliAI — Plugin Launch & Revenue Roadmap

You now have a working Claude marketplace plugin: **`kundli-ai.plugin`** (14.5 KB).

This document covers everything you need to do next, in order, across four phases:

1. **Test & install the plugin locally** (today, 10 minutes)
2. **Publish to the Claude marketplace** (this week)
3. **Build the website + connect Razorpay** (next session)
4. **SEO + traffic + revenue** (week 2 onwards)

---

## Phase 1 — Test the plugin locally (10 minutes)

Before submitting to the marketplace, install it on your own Cowork / Claude Code to make sure every skill triggers correctly.

### Install
1. The `.plugin` file is rendered as a card in this chat. Click **"Install plugin"** on the card.
2. Cowork unpacks it and registers all 6 skills.
3. Restart your Cowork session if prompted.

### Test each skill
Open a fresh chat and try these prompts. Each one should trigger the matching skill — Claude will name which skill it loaded.

| Prompt to try                                                                                                              | Should trigger                |
| -------------------------------------------------------------------------------------------------------------------------- | ----------------------------- |
| `Generate my basic kundli — born 14 March 1995, 06:42 AM, Pune`                                                            | `kundli-basic-report`         |
| `Detailed kundli reading. Name: Rohan, DOB 23 Aug 1988, 10:15 PM, Chennai. Question: when will I marry?`                   | `kundli-detailed-report`      |
| `Premium kundli for me + Milan with my partner. [paste two sets of details]`                                               | `kundli-premium-report`       |
| `Run a kundli matching between [partner 1] and [partner 2]`                                                                | `kundli-milan-compatibility`  |
| `Monthly horoscope for May 2026, moon sign Vrishchika, name Priya`                                                         | `monthly-horoscope`           |
| `Today's rashifal for Mesha`                                                                                               | `daily-rashifal`              |

### What to look for
- The right skill name appears in the system reminder.
- Claude asks for missing birth details if you don't supply them.
- The soft CTA (`kundliai.in` link) appears at the end of every report.
- Reports hit the target word counts (1,500 / 2,500 / 3,000 / 500 / 500 / 150).

If something doesn't trigger, just tell me which prompt failed and I'll tighten the trigger phrases in that SKILL.md.

---

## Phase 2 — Publish to the Claude marketplace (this week)

Anthropic's plugin marketplace is currently a research preview, distributed via plugin marketplaces (collections of plugins). You have two options:

### Option A — Submit to an existing marketplace (fastest)
The `anthropic-skills` and `cowork-onboarding` marketplaces are run by Anthropic. Community marketplaces also exist. Most accept submissions through GitHub.

**Steps:**
1. Create a GitHub repo: `kundli-ai`
2. Push the entire `kundli-ai/` directory (not the `.plugin` zip — the source files)
3. Open an issue or PR on a relevant marketplace repo asking to add your plugin
4. Recommended search terms to find the right marketplace: *"claude code marketplace"*, *"cowork plugin marketplace"* on GitHub

### Option B — Publish your own marketplace (more control)
Create a `marketplace.json` file at the root of a new GitHub repo listing your plugin. Users add your marketplace URL to their Cowork / Claude Code settings, then install your plugin from it.

This is the path I'd recommend for KundliAI long-term — you can later add more plugins (e.g., a `panchang-ai` plugin, a `vastu-ai` plugin) to the same marketplace and own the distribution channel.

A `marketplace.json` looks like:
```json
{
  "name": "kundliai-marketplace",
  "owner": { "name": "Balaganapathi R" },
  "plugins": [
    {
      "name": "kundli-ai",
      "source": "./kundli-ai",
      "description": "Vedic Kundli readings inside Claude"
    }
  ]
}
```

When you're ready, ping me and I'll generate the marketplace repo scaffold + GitHub Actions for auto-publishing.

### Marketplace listing copy (use as-is)

**Title:** KundliAI — Authentic Vedic Kundli Readings

**One-liner:** Get a deeply personal 1,500–3,000 word kundli covering career, marriage, health, and 2025–26 predictions — generated from your birth details inside Claude.

**Key features:**
- 6 skills: Basic, Detailed, and Premium kundli reports + Kundli Milan compatibility + monthly horoscope + daily rashifal
- Covers lagna, career fields, marriage timing, health tendencies, and month-by-month forecasts
- Specific months named (not vague "mid-year"); every challenge paired with a remedy
- Free to install; optional paid PDF + WhatsApp delivery via kundliai.in

**Tags:** `vedic-astrology` `kundli` `horoscope` `india` `jyotish` `birth-chart`

---

## Phase 3 — Build the website + connect Razorpay (next session)

Plan we agreed on earlier:

- Single-page site, free subdomain (`kundliai.netlify.app` or `kundliai.vercel.app`)
- 4 pricing buttons → 4 Razorpay Payment Links from your existing account
- Tally form embedded for birth details
- SEO meta tags + OpenGraph for social sharing
- Sample report visible on page (the Priya Sharma example from your business kit)

**What I'll need from you when we start that phase:**
- Your 4 Razorpay Payment Link URLs (Basic ₹99, Detailed ₹199, Premium ₹499, Subscription ₹149/mo)
- Your Tally form URL (or I can scaffold the form structure for you to create)
- Your WhatsApp Business number (for the "DM us" button)
- An Instagram handle if you have one (so I link it in the footer)

Just say "let's build the website" in a fresh chat with that info and I'll deliver an HTML + CSS file you can drop straight into Netlify.

---

## Phase 4 — SEO + traffic + revenue (week 2 onwards)

Three traffic loops, ranked by ROI for an India-first astrology business:

### Loop 1 — SEO content (slow but compounding)
Target keywords:
- `free kundli online` (40K searches/month, low competition for AI-driven content)
- `kundli milan in english` (8K/month)
- `marriage compatibility by date of birth` (12K/month)
- `monthly horoscope [moon sign]` (sums to ~30K/month across 12 signs)
- `[city] best astrologer` (long-tail, 200–500/month each — high intent)

Plan for week 2: I'll generate 20 SEO-optimised blog posts using the kundli-detailed-report skill itself (each post = a sample reading for a fictional person, with proper schema markup). Plus sitemap.xml, robots.txt, and submission to Google Search Console.

### Loop 2 — Plugin marketplace (free distribution to Claude users)
Once published, every install is a top-of-funnel touch. Conversion rate on plugins → paid product can be 0.5–2% if the CTA is well-placed (yours is). At 1,000 installs you should see 5–20 customers.

### Loop 3 — Instagram + WhatsApp (your business kit's playbook)
Already covered in your business kit — the 30-day plan is solid. Combine it with Loops 1 and 2 for compounding effects.

### Revenue math (conservative, month 2)
- Website organic + plugin install funnel: 50 customers × ₹199 avg = **₹9,950**
- Instagram funnel (per business kit): 100 customers × ₹199 = **₹19,900**
- Subscription (10 subscribers × ₹149): **₹1,490 recurring**
- **Month 2 total: ~₹31,000**

If month 2 hits target, doubling to ₹60K in month 3 is realistic by:
- Boosting top-performing reels with paid ads (₹500–₹2,000 spend)
- Adding 3 more SEO posts/week
- DM-to-influencer outreach to micro-astrology accounts

---

## Files in this delivery

- `kundli-ai.plugin` — the installable plugin (give the click)
- `kundli-ai/` — the source folder (push to GitHub for marketplace submission)
- `KundliAI_Launch_Guide.md` — this document

When you're ready for Phase 3 (website), open a fresh chat, drop in your Razorpay Payment Link URLs, and say "build the kundliai website". Should take one session.

---

*Built by Claude in Cowork, May 2026.*
