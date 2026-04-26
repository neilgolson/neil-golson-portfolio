# neilgolson.com — Claude Code Briefing Doc
# Generated from design session — April 2026
# Use this as the single source of truth for the build

---

## Project overview

Portfolio site for Neil Golson — VP, Brand & Creative at Realtor.com.
Targeting CMO / SVP Brand/Marketing roles at Fortune 500 companies.
Primary markets: Charlotte, NC (Lowe's, Bank of America, Truist) and Atlanta, GA.

Site is currently hosted on GitHub Pages at neilgolson.com.
Current state: Panic Predictor app lives at neilgolson.com (root).
HeardIt lives at heardit.neilgolson.com/dashboard.

The v4 HTML file (neilgolson_v4.html) is the approved design.
Task: implement it, then build out individual case study pages.

---

## Design system

Font stack:
- Display: Playfair Display (Google Fonts) — serif, used for headlines and section titles
- Body: DM Sans (Google Fonts) — clean, modern sans

Color palette:
- --ink: #1a1814 (near-black warm)
- --paper: #f5f2ec (warm off-white — page background)
- --warm-white: #faf8f4 (slightly lighter, used for panels)
- --mid: #6b6560 (muted body text, secondary)
- --light: #9b9590 (labels, captions, tertiary)
- --accent: #c2410c (burnt orange — CTAs, eyebrows, rules)
- --border: rgba(26,24,20,0.12)
- --border-strong: rgba(26,24,20,0.25)

Aesthetic: editorial/authoritative. Think The Atlantic meets a senior executive's calling card.
NOT a creative director showreel. NOT an agency portfolio.
Everything earns its place. Generous whitespace. 0.5px borders throughout.
No gradients, no shadows, no rounded corners (border-radius: 3px max on containers).

---

## Site structure

```
neilgolson.com/              ← main portfolio page (index.html)
neilgolson.com/work/realtor  ← case study 1
neilgolson.com/work/tesla    ← case study 2
neilgolson.com/work/flash    ← case study 3
neilgolson.com/work/coke     ← case study 4
neilgolson.com/work/mission-zero ← case study 5 (standalone — enough assets)
```

heardit.neilgolson.com/dashboard ← separate subdomain, already live, don't touch

---

## Main page — remaining placeholders to fill

### Headshot
Already wired in via LinkedIn CDN URL. If that URL expires, replace with:
`<img src="/assets/neil-headshot.jpg">` (upload headshot to /assets/)

LinkedIn URL (may expire):
https://media.licdn.com/dms/image/v2/D5603AQFeyDcPHybY7g/profile-displayphoto-crop_800_800/B56ZojGDDtI4AI-/0/1761525380374?e=1778716800&v=beta&t=Mmhwo-2p1RnBz_kpu8S8Cf8JzLVuKVgz4LsQERR56a4

### Contact email
Replace: neil@neilgolson.com → **Neil's actual email TBD**

### Resume PDF
Replace href="#" on the Download Resume CTA with the hosted PDF path.
Suggest: /assets/neil-golson-resume.pdf

### Case study media — what's wired vs still needed

| Case study | Video embed | Status |
|---|---|---|
| Realtor.com / Reba | YouTube ID: 2QLaJFOebvY | ✅ ready to embed |
| Mission Zero | YouTube ID: R6OW89Dr5Ew (long) + 4hjz2R426ng (short) | ✅ ready — use long on main page |
| FLASH | No video — use IPMI article as press link | ✅ use article link |
| Tesla/SolarCity | No video — use Electrek articles + photos | ✅ use article links |

### App screenshots (Built section)
Two dashed placeholders need replacing with actual screenshots:
- Panic Predictor: take screenshot of neilgolson.com, save as /assets/panic-predictor-screenshot.jpg
- HeardIt: take screenshot of heardit.neilgolson.com/dashboard, save as /assets/heardit-screenshot.jpg
Replace the `.app-ph` divs with: `<img src="/assets/[filename]" alt="[App name]">`

### Press grid — 4 items, currently 2 real + 2 placeholder
Real items already wired:
1. PR Newswire — SXSW 2026 lineup → https://www.prnewswire.com/news-releases/welcome-to-our-open-house-realtorcom-announces-sxsw-2026-line-up-302693759.html
2. Effie Awards 2025 — Finalist (no URL yet, leave as is)

Replace the 2 blank press items with:
3. AdExchanger (March 2026) — "How Realtor.com Is Using AI Creative To Expand Its Ad Footprint" → https://www.adexchanger.com/ai/how-realtor-com-is-using-ai-creative-to-expand-its-ad-footprint/
4. IPMI / Parking & Mobility — "From Tesla to Parking: An Executive's Bold Move" → https://www.parking-mobility.org/blog/from-tesla-to-parking/

### SXSW panel 2 — currently no video, just LinkedIn link
If YouTube ID becomes available, replace the LinkedIn link section with:
`<iframe src="https://www.youtube.com/embed/[VIDEO_ID]" ...>`
BrandComms.ai LinkedIn post: https://www.linkedin.com/posts/brandcomms-ai_sxsw-2026-highlight-helping-teams-with-activity-7439496589796270080-9t6i/

---

## Case study pages — full asset inventory

### CASE STUDY 1: Realtor.com Brand Relaunch
File: /work/realtor/index.html
Slug: /work/realtor

**The story:** Repositioned a 30-year-old brand around trust and expertise while
under unprecedented competitive assault (Homes.com 10× outspend, Zillow 4×).
Built the business case for celebrity, negotiated Reba McEntire deal, built
campaign from brief to air with GSD&M. Simultaneously rebuilt internal agency of
30+ and managed $50M brand + $100M performance budgets.

**Metrics:**
- +20% CPIV improvement
- 5 consecutive quarters of YoY revenue growth
- 7+ months of brand health improvement streak
- Effie Finalist 2025
- $143M revenue in most recent quarter (+10% YoY)
- 3.4× visit share vs Homes.com (Comscore)
- Closed >50% of visit share gap vs Zillow in 18 months

**Assets:**
- Reba :30 TV spot → YouTube: 2QLaJFOebvY
- Realtor.com+ product launch → YouTube: jgywhxfOOvw
- Realtor.com+ press release → https://www.prnewswire.com/news-releases/realtorcom-unveils-realtorcom-a-first-of-its-kind-collaborative-home-search-experience-302666863.html
- Seller AI ad → AdExchanger: https://www.adexchanger.com/ai/how-realtor-com-is-using-ai-creative-to-expand-its-ad-footprint/
- Seller AI :30 spot → YouTube: TBD (Neil to provide)
- SXSW Nearly Home panel → YouTube: HmSvdU2-qlc
- SXSW PR Newswire → https://www.prnewswire.com/news-releases/welcome-to-our-open-house-realtorcom-announces-sxsw-2026-line-up-302693759.html
- BrandComms.ai SXSW highlight → https://www.linkedin.com/posts/brandcomms-ai_sxsw-2026-highlight-helping-teams-with-activity-7439496589796270080-9t6i/
- Effie Awards 2025 — Finalist (no URL yet)

**Suggested page structure:**
1. Hero: title + the competitive context (10× outspend framing)
2. The challenge: what the brand looked like before
3. The insight: trust and expertise as the differentiator, not price or features
4. The work: Reba spot embed → Realtor.com+ launch video → Seller AI ad
5. The SXSW chapter: storytelling panel + BrandComms.ai highlight
6. Results: metrics block
7. Press: AdExchanger + PR Newswire + Effie

---

### CASE STUDY 2: Mission Zero
File: /work/mission-zero/index.html
Slug: /work/mission-zero

**The story:** Built a first-of-its-kind industry coalition to address veteran
homelessness. United Realtor.com with Veterans United and industry partners.
Designed campaign architecture that gave the brand a social mission without
losing commercial credibility. Every purpose dollar tracked against brand health
and conversion outcomes.

**Assets:**
- Mission Zero long-form → YouTube: R6OW89Dr5Ew
- Mission Zero short → YouTube: 4hjz2R426ng

**Suggested page structure:**
1. Hero: the problem (veteran homelessness + housing industry's role)
2. The coalition model: why industry partnership vs brand-solo
3. The creative: long-form video embed
4. How it was measured: dual KPI model (brand health + conversion)
5. Short-form video (second embed — show both versions)
6. Results TBD (Neil to provide any metrics)

---

### CASE STUDY 3: Tesla / SolarCity
File: /work/tesla/index.html
Slug: /work/tesla

**The story:** Two parallel acts. At Tesla: redesigned the in-store retail
experience to integrate home energy into the Model 3 purchase journey — achieved
30%+ attachment rate. At SolarCity: built a 1,500-person field marketing and lead
gen operation, scaled market share from 26% to 37%, national retail partnerships
with Home Depot, Best Buy, BMW, AT&T, DIRECTV. The Home Depot partnership is
especially significant given Lowe's as primary target employer.

**Metrics:**
- 30%+ energy/solar attachment on Model 3 purchases
- Market share: 26% → 37%
- Install volume: 3×
- 800 Home Depot store presence (Electrek, Feb 2018)

**Assets:**
- Electrek — "Tesla's solar division is expanding to 800 Home Depot stores" (Feb 2018) → https://electrek.co/2018/02/01/tesla-solar-sale-home-depots/
- Electrek — "Tesla solar branded panels in-store" (Jun 2017) → https://electrek.co/2017/06/25/tesla-solar-branded-solar-panels-store/
- IPMI magazine cover feature with Neil's photo in front of Tesla → https://www.parking-mobility.org/blog/from-tesla-to-parking/
  NOTE: This article is the bridge from Tesla to FLASH. Use on Tesla page
  with a link forward to the FLASH case study.

**Suggested page structure:**
1. Hero: the insight ("selling a $100K decision at the same moment as a $0.99 one")
2. The Tesla chapter: retail redesign, Model 3 attachment rate
3. The SolarCity chapter: field org, CAC reduction, Home Depot partnership
4. Press: both Electrek articles (embed screenshots or link cards)
5. The bridge: "What I learned building this led directly to the next chapter" → link to FLASH

---

### CASE STUDY 4: FLASH / FlashParking
File: /work/flash/index.html
Slug: /work/flash

**The story:** Joined as CMO when the category didn't exist as a defined market.
Named the category, built go-to-market from scratch across B2G/B2B2C — cities,
parking operators, enterprise accounts. Proved government buyers respond to brand
as much as procurement specs. $300M PE-backed outcome.

**Metrics:**
- Market share: <1% → 33%
- $300M PE outcome

**Assets:**
- IPMI / Parking & Mobility magazine cover feature (Neil on cover in front of Tesla)
  → https://www.parking-mobility.org/blog/from-tesla-to-parking/
  Headline: "From Tesla to Parking: An Executive's Bold Move"
  NOTE: This article is the best asset on the page — let the press headline lead.
  The photo of Neil in front of a Tesla with FlashParking branding is extraordinary.

**Suggested page structure:**
1. Hero: "From Tesla to Parking: An Executive's Bold Move" — let the press write it
2. The category problem: parking tech had no category leader, no brand language
3. What was built: naming, positioning, go-to-market architecture
4. The B2G insight: government buyers respond to brand, not just specs
5. Results: market share and PE outcome
6. Press: IPMI feature prominently — pull quote + link + image of magazine cover if available

---

### CASE STUDY 5: Coca-Cola
File: /work/coke/index.html
Slug: /work/coke

**The story:** Seven years at the world's most valuable brand, spanning four
distinct roles — brand manager on citrus portfolio (Vault, Mello Yello, Fanta,
Fresca), brand manager on Coca-Cola core (Super Bowl, Olympics, cultural
campaigns), international supply chain and business development in Shanghai
(McDonald's global account), and senior brand manager driving first US market
share growth in seven years.

This case study is the foundation chapter — it shows range, cultural ambition,
and brand craft at massive scale before the CMO years.

**Key narrative beats:**
- Vault: kept the brand at $0.99 by engineering bottle from 20oz to 16oz and
  selling bottlers on the operational investment. Commodity brand management
  at its most creative.
- White Can: helped introduce the limited-edition white Coca-Cola can for the
  WWF Arctic Home campaign. Now in the Smithsonian collection.
- Super Bowl: Polar Bowl campaign (Cannes submission)
- Olympics 2012: Jessica Long paralympian campaign
- American Idol: Taio Cruz integration
- McDonald's global: Shanghai posting, AMPEA Olympics glasses promotion,
  earned Global Benchmark Supplier designation for McDonald's division
- Mini Can: introduced 100-calorie mini-can + redesigned grocery merchandising
  strategy. First US market share growth in 7 years.

**Assets:**

Vault:
- Vault TV spot → YouTube: QwrEpYXcobc

White Can / Arctic Home:
- Smithsonian artifact page → https://www.si.edu/object/white-coca-cola-can%3Anmah_1421965
- Arctic Home campaign → https://www.thearcticinstitute.org/coca-cola-world-wildlife-fund-arctic-home/

Super Bowl:
- Polar Bowl Cannes submission → YouTube: SLWPYdsV7po

Olympics:
- Jessica Long paralympian TV spot → https://www.ispot.tv/ad/7V8H/the-coca-cola-company-olympics-featuring-jessica-long

American Idol:
- Taio Cruz performance/integration → YouTube: aRWvfDOsjWQ

McDonald's AMPEA:
- Olympic Glasses promotion TV spot → YouTube: Zwk-SfR69Uw

Mini Can:
- BevNET — "Coca-Cola Cuts Price on 8-Pack of Mini Cans" → https://www.bevnet.com/news/2011/coca-cola-cuts-price-on-8-pack-of-mini-cans

**Suggested page structure:**
1. Hero: "Seven years at the world's most valuable brand. Four different jobs.
   One consistent question: how do you make people feel something about a product
   they've already decided they love?"
2. The Vault chapter: commodity brand management — keep it at $0.99 through
   operational creativity. Video embed.
3. The cultural moments chapter: Super Bowl (Polar Bowl embed) +
   Olympics (Jessica Long) + American Idol (Taio Cruz). Grid of three.
4. The coalition chapter: White Can + Arctic Home + WWF. Smithsonian link as
   the proof point — a product you worked on is in a museum.
5. The international chapter: Shanghai, McDonald's Global Benchmark Supplier,
   AMPEA Olympics spot.
6. The Mini Can chapter: 100-calorie format + grocery redesign = first US market
   share growth in 7 years. BevNET link.

---

## Case study page template (HTML structure to reuse)

Each case study page should:
- Share the same nav, footer, fonts, and CSS variables as the main page
- Have a back arrow → "← All work" linking to neilgolson.com/#work
- Use the same --paper background and editorial type system
- Follow this rough structure:

```
<nav> (same as main page + back link)

<section class="cs-hero">
  [eyebrow: company + category tag]
  [h1: case study title]
  [2-sentence context paragraph]
  [metrics bar: 3-4 key numbers]
</section>

<section class="cs-body">
  [narrative sections with video embeds and press link cards interspersed]
</section>

<section class="cs-press">
  [press grid — same component as main page]
</section>

<section class="cs-nav">
  [← Previous case study] [Next case study →]
</section>

<footer> (same as main page)
```

Press link cards (reusable component):
```html
<a class="press-card" href="[URL]" target="_blank">
  <div class="press-card-outlet">[Outlet name]</div>
  <div class="press-card-hed">[Article headline]</div>
  <div class="press-card-arrow">↗</div>
</a>
```

Video embed (reusable component — 16:9):
```html
<div class="video-wrap">
  <iframe
    src="https://www.youtube.com/embed/[VIDEO_ID]"
    title="[Title]"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
```

CSS for video-wrap:
```css
.video-wrap {
  position: relative;
  padding-bottom: 56.25%;
  height: 0;
  overflow: hidden;
  border-radius: 3px;
  background: #1a1814;
  margin: 2rem 0;
}
.video-wrap iframe {
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  border: none;
}
```

---

## Build priority order

1. Wire remaining placeholders into main index.html (app screenshots, press items, email, resume link)
2. Build /work/realtor — highest-stakes case study, most assets
3. Build /work/mission-zero — simplest, two videos, clean story
4. Build /work/tesla — Electrek press + metrics
5. Build /work/flash — IPMI cover as hero asset
6. Build /work/coke — most complex, most assets, most video embeds

---

## Assets still outstanding (Neil to provide)

- [ ] Seller AI :30 YouTube ID
- [ ] Real email address for contact section
- [ ] Resume PDF (upload to /assets/ or external host)
- [ ] Coke/McDonald's AMPEA spot confirmed working: youtube.com/watch?v=Zwk-SfR69Uw
- [ ] Any Effie Awards public URL
- [ ] App screenshots for Panic Predictor + HeardIt (take these in browser)
- [ ] Confirm actual SXSW panel titles for the two panels

---

## Voice and tone guide (for any copy Claude Code writes)

Neil's locked executive summary (use verbatim in hero):
"I've spent 25 years at the intersection of brand and the moment someone decides
to act — a $0.99 Coke from a Home Depot cooler, a $100,000-plus Tesla with solar,
a multi-million-dollar parking infrastructure contract. The psychology of trust
looks different at every scale. Building for all of it is the through-line of
my career."

Closing line (use in contact section):
"I do my best work where the stakes are real and brand is expected to earn its
place in the P&L."

Tone: warm but authoritative. Confident without being boastful. Metrics-backed
but human. No buzzwords. No "leveraged synergies." No "passionate about brand."
If a sentence could appear in a McKinsey deck, rewrite it.

The career diversity is a narrative asset, not a liability. The through-line is:
understanding how humans make trust-based purchase decisions at every scale —
from $0.99 to $100K to multi-million-dollar B2G contracts.

Primary target audience reading this site: Lowe's CMO search committee,
Charlotte/Atlanta Fortune 500 CHROs, Korn Ferry/Spencer Stuart search partners.
Secondary: anyone who Googles Neil's name after seeing his resume.

